# json 文件操作相关的问题，库

## 链接
- JSON风格指南 by Google https://github.com/darcyliu/google-styleguide/blob/master/JSONStyleGuide.md

## Python
```python
import json

json.dumps(d, 
   sort_keys=True, # 排序 
   ensure_ascii=False,  # 显示 unicode,  如果是 True, 那么就强制使用 ascii， 汉字会被编码成 \uXXX 的格式
   indent=2, # 带换行，2个空格
)
```

## Java

### fastjson
- 格式化，保存时排序
- SerializerFeature.PrettyFormat 这个是可读，带换行，4个空格 （否则不带换行）
- SerializerFeature.SortField.MapSortField （这个可以排序所有的 kv），很多文档只给了 SerializerFeature.SortField，这个不管用

```java
private static void prettyWriteJsonObjectToFile(String path, JSONObject jsonObject) {
      String formattedJsonString = JSON.toJSONString(
              jsonObject,
              SerializerFeature.PrettyFormat,
              SerializerFeature.SortField.MapSortField
      );
      try {
          Files.write(Paths.get(path), formattedJsonString.getBytes(StandardCharsets.UTF_8));
      } catch (IOException e) {
          e.printStackTrace();
      }
  }
```

### Gson
- 如果想格式完全和 python 对齐， fastjson 不太行， ： 前面会多个空格
- 可以用 Gson, 默认格式是2空格，其他格式和 python 一样

```java
private static String stringPrettyString(String json) { // 兼容 Object 和 Array
    JsonElement jsonElement = new JsonParser().parse(json);
    Gson gson = new GsonBuilder()
                  .disableHtmlEscaping() // 为了显示 utf8 汉字，否则会编码成 \uXXX
                  .setPrettyPrinting() // 优美格式，2个空格，否则不会换行
                  .create();
    return gson.toJson(jsonElement);
}

```
