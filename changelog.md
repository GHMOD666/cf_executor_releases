# CF Executor v5.8 安全加固版

🔒 密钥前后端分离 (daemon签名, 前端不持有密钥)
🔒 修复命令注入 (token校验 + customPath过滤器)
🔒 修复 XSS (日志输出HTML转义)
🔒 修复完整性校验 (哈希移至daemon端)
🔒 权限收紧 (0700/0600)
🔒 在线复检 fail-close
🔒 jj 每次执行前校验SHA256 (mtime缓存)
✅ 卡密可选记住复选框
⚡ 崩溃重启指数退避 (3s→6s→12s→max 60s)
⚡ check_cfm 降频 3s→10s
⚡ inotify 替代轮询 (pipe_exec/pipe_stop)
⚡ 自适应轮询 200ms→2s 降频
⚡ 脚本执行超时 300s 自动kill
⚡ 屏幕闪烁 max_brightness 适配
📋 security_check 记录退出原因
📋 Loading 超时提示 (5s无响应)
📋 版本号统一为 v5.8
⚠️ 修复 --sign 路径导致密钥验证失败
