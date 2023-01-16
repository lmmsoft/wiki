# 本文记录网络相关的biji

## 服务器推送技术 Push technology
- https://en.wikipedia.org/wiki/Push_technology
- https://zh.wikipedia.org/wiki/%E6%8E%A8%E9%80%81%E6%8A%80%E6%9C%AF
- publish/subscribe 模型
  - 邮件推送
    - SMTP 协议是一个推送协议
    - POP3 或 IMAP 是 pull 协议
    - IMAP 协议包括 IDLE command， 可以推送
  - 网页推送
    -  HTTP2 版本的去即时的事件
  -  HTTP服务器推送
    - 一些 HTML5 的 WebSocket API 允许 Web 服务器和客户端，通过 TCP 全双工通信进行交流
  - 推送技术
    - 持久的 HTTP 协议，使得响应永久打开
  - 长轮询
    - 长轮询本身并不是一个真正的推送；长轮询是传统轮询技术的一种变体，但是它允许在一个真正的推送不可能的情况下模拟推送机制，例如安全策略的网站需要阻止的HTTP/S请求
    - 长轮询， 客户端从服务器请求消息与正常轮询完全相同，但正如你预料到的，服务器可能不会立即回应。当收到轮询时如果服务器的客户端没有新的消息，不是发送一个空的响应，服务器端公开请求并等待成为有用的响应消息。一旦它获得新的消息，服务器会立即向客户端发送 HTTP/S 的响应，完成开放 HTTP 的请求。收到服务器响应后，客户端通常会立即发出另一个服务器的请求
    -  XMPP
