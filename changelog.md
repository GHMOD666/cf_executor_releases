# v10.1 更新内容

- 安全升级: MD5→SHA256 完整性校验
- 安全升级: daemon --verify 代理模式, 卡密不再暴露于 shell
- 安全升级: keyt.cn 请求 HMAC 签名防伪造
- 安全升级: 验证按钮 5 秒冷却
- 安全升级: localStorage 卡密数据 AES 加密存储
- 安全升级: 字符串加密 XOR→S-box+XOR+轮转
- 多项 Bug 修复与稳定性提升