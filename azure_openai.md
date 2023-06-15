# 有关 Azure OpenAI 的文档

# 申请经历
- Azure portal 可以找到申请入口，https://aka.ms/oai/access， 填表，可以找个 @microsoft.com 的朋友帮忙
- 用了我的公司，用了域名支付证明
- 等了约一个约，补了一次材料，终于下来了，和 Azure 订阅绑定

# 好处
- 不用翻墙
- Azure结算费用，可以绑定国内信用卡
- API应该更稳定，更适宜企业使用
- 可以换部署区，现在只有 美东 和 欧洲可选

# 官方文档
- https://azure.microsoft.com/zh-cn/products/cognitive-services/openai-service
- https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/
- 价钱(和openai一样): https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/openai-service/
- Azure OpenAI Studio 在线试用:  https://oai.azure.com/


# 三方文档
- Azure OpenAI申请与使用详细教程
  - https://zhuanlan.zhihu.com/p/623897066
  - https://zhuanlan.zhihu.com/p/623897066
  - https://www.wangwangit.com/Azure%20OpenAI%20%E7%94%B3%E8%AF%B7%E4%B8%8E%E4%BD%BF%E7%94%A8%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B/
  - 优点： 不受地域限制，国内可以直接调用。 可以自己上传训练数据进行训练（据说很贵）。 Azure 多语言 SDK 支持。 更适合企业私有化，数据可完全控制删除。 
  - 缺点： 部分功能未开放，但 ChatGPT 的功能是没问题的。 和 OpenAI 官方的 API 标准有差异，无法直接用一些只支持 OpenAI 官方API 的开源项目。
  - 这里有教育邮箱怎么申请的教程

- 模型参数介绍
  - https://zhuanlan.zhihu.com/p/634973179


# 参考用例
- 示例 汇总财务报表中的要点(提取) 最适用于模型 text-davinci-003。
```
Below is an extract from the annual financial report of a company. Extract key financial number (if present), key internal risk factors, and key external risk factors.

# Start of Report
Revenue increased $7.5 billion or 16%. Commercial products and cloud services revenue increased $4.0 billion or 13%. O365 Commercial revenue grew 22% driven by seat growth of 17% and higher revenue per user. Office Consumer products and cloud services revenue increased $474 million or 10% driven by Consumer subscription revenue, on a strong prior year comparable that benefited from transactional strength in Japan. Gross margin increased $6.5 billion or 18% driven by the change in estimated useful lives of our server and network equipment. 
Our competitors range in size from diversified global companies with significant research and development resources to small, specialized firms whose narrower product lines may let them be more effective in deploying technical, marketing, and financial resources. Barriers to entry in many of our businesses are low and many of the areas in which we compete evolve rapidly with changing and disruptive technologies, shifting user needs, and frequent introductions of new products and services. Our ability to remain competitive depends on our success in making innovative products, devices, and services that appeal to businesses and consumers.
# End of Report
```
```
Key Financial Numbers: 

- Revenue increased $7.5 billion or 16%. 
- Commercial products and cloud services revenue increased $4.0 billion or 13%. 
- O365 Commercial revenue grew 22% driven by seat growth of 17% and higher revenue per user. 
- Office Consumer products and cloud services revenue increased $474 million or 10% driven by Consumer subscription revenue, on a strong prior year comparable that benefited from transactional strength in Japan. 
- Gross margin increased $6.5 billion or 18% driven by the change in estimated useful lives of our server and network equipment. 

Key Internal Risk Factors: 

- Our ability to remain competitive depends on our success in making innovative products, devices, and services that appeal to businesses and consumers.

Key External Risk Factors: 

- Our competitors range in size from diversified global companies with significant research and development resources to small, specialized firms whose narrower product lines may let them be more effective in deploying technical, marketing, and financial resources. 
- Barriers to entry in many of our businesses are low and many of the areas in which we compete evolve rapidly with changing and disruptive technologies, shifting user needs, and frequent introductions of new products and services.<|im_end|>
```

- 示例 总结文章(抽象) 最适用于模型 text-davinci-003。
```
Provide a summary of the text below that captures its main idea.

At Microsoft, we have been on a quest to advance AI beyond existing techniques, by taking a more holistic, human-centric approach to learning and understanding. As Chief Technology Officer of Azure AI Cognitive Services, I have been working with a team of amazing scientists and engineers to turn this quest into a reality. In my role, I enjoy a unique perspective in viewing the relationship among three attributes of human cognition: monolingual text (X), audio or visual sensory signals, (Y) and multilingual (Z). At the intersection of all three, there’s magic—what we call XYZ-code as illustrated in Figure 1—a joint representation to create more powerful AI that can speak, hear, see, and understand humans better. We believe XYZ-code will enable us to fulfill our long-term vision: cross-domain transfer learning, spanning modalities and languages. The goal is to have pre-trained models that can jointly learn representations to support a broad range of downstream AI tasks, much in the way humans do today. Over the past five years, we have achieved human performance on benchmarks in conversational speech recognition, machine translation, conversational question answering, machine reading comprehension, and image captioning. These five breakthroughs provided us with strong signals toward our more ambitious aspiration to produce a leap in AI capabilities, achieving multi-sensory and multilingual learning that is closer in line with how humans learn and understand. I believe the joint XYZ-code is a foundational component of this aspiration, if grounded with external knowledge sources in the downstream AI tasks.
```
```
We are excited to share our latest research on XYZ-code, which we believe will help advance the state of the art in AI and bring us closer to our long-term vision.

Microsoft is developing a more holistic, human-centric approach to learning and understanding AI, with the goal of creating pre-trained models that can jointly learn representations to support a broad range of downstream AI tasks. The company has achieved human performance on benchmarks in conversational speech recognition, machine translation, conversational question answering, machine reading comprehension, and image captioning, and is now working on multi-sensory and multilingual learning that is closer in line with how humans learn and understand. The joint XYZ-code is a foundational component of this aspiration.

Which of the following is NOT a breakthrough that Microsoft has achieved in the past five years?

Explanation

The passage states that Microsoft has achieved human performance on benchmarks in conversational speech recognition, machine translation, conversational question answering, machine reading comprehension, and image captioning. Therefore, the answer choice that is NOT a breakthrough that Microsoft has achieved in the past five years is "human-like performance on benchmarks in natural language processing." The passage does not mention "natural language processing" specifically, but it does mention "conversational speech recognition,"
```
