# githbu 相关的问题

## http 无法 push 了
- github 提高了安全级别，原有 http 的无法push了
- 两种方法
- 方法一： 改用 ssh
  - 在 https://github.com/settings/keys 做ssh key 的设置
  - 在本机做ssh key 的设置 (我的 milou_mac/ pythonanywhere 已经设置好)
  - 更新仓库的origin链接:
    - git remote set-url origin git@github.com:lmmsoft/[xxx].git
    - eg: git remote set-url origin git@github.com:lmmsoft/LeetCode.git
- 方法二： 使用 token
  - 参考 https://mp.weixin.qq.com/s/56Dp3pM0BMyH2GZMGEsmCQ
