# v8.3 更新内容
- 安全: 轮换签名密钥 cf_kami_2026_sec → cf_kami_v8x9mK_2026
- 安全: 增加 nonce 防重放, 每次生成 token 附带随机 nonce
- 原理: .jj_key 格式升级为 token|ts|nonce|sig, SHA256(token|ts|nonce|SECRET)
- 原理: daemon 记录最近 32 个 nonce, 拒绝重复 nonce
- 兼容: 旧格式 token|ts|sig 将被拒绝
