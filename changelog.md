# v10.2 安全升级

- Nonce 防重放: 32→256 槽位 + 磁盘持久化 (daemon 重启不丢失)
- 日志脱敏: 卡密/设备ID 自动掩码
- update.json 签名验证: HMAC-SHA256 防 MITM 篡改
- CSP 安全头: 限制脚本/样式/连接来源
- 验证频率限制: 5次/10分钟 防暴力破解
- 崩溃恢复强化: 速率限制 + 健康检查 + nonce 清理

# v10.1 安全升级

- 安全升级: MD5→SHA256 完整性校验
- 安全升级: daemon --verify 代理模式, 卡密不再暴露于 shell
- 安全升级: keyt.cn 请求 HMAC 签名防伪造
- 安全升级: 验证按钮 5 秒冷却
- 安全升级: localStorage 卡密数据 AES 加密存储
- 安全升级: 字符串加密 XOR→S-box+XOR+轮转
- 多项 Bug 修复与稳定性提升