# json 文件操作相关的问题，库

## Java

## fastjson
- 格式化，保存时排序
- SerializerFeature.PrettyFormat 这个是可读，带换行，4个空格 （否则不带换行）
- SerializerFeature.SortField.MapSortField （这个可以排序所有的 kv），很多文档只给了 SerializerFeature.SortField，这个不管用
```
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

## Gson
- 如果想格式完全和 python 对齐， fastjson 不太行， ： 前面会多个空格
- 可以用 Gson, 默认格式是2空格，其他格式和 python 一样

```
private static String stringPrettyString(String json) { // 兼容 Object 和 Array
    JsonElement jsonElement = new JsonParser().parse(json);
    Gson gson = new GsonBuilder().disableHtmlEscaping().setPrettyPrinting().create();
    return gson.toJson(jsonElement);
}

```
