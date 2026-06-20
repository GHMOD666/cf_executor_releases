# CF Executor v6.1 安全加固版

## 安全加固
- 密钥前后端分离 (daemon 签名, 前端不持有密钥)
- 修复命令注入漏洞 (token 校验 + customPath 过滤器)
- 修复 XSS 漏洞 (日志输出 HTML 转义)
- 修复完整性校验 (哈希移至 daemon 端)
- 权限收紧 (0700/0600, 拒绝非 root 访问)
- 在线复检 fail-close (禁用卡密后需联网验证)
- jj 每次执行前校验 SHA256 (mtime 缓存)

## 功能改进
- 卡密可选记住 (勾选复选框后才保存)
- 脚本执行超时 300s 自动 kill
- 自适应轮询 200ms 降频至 2s
- check_cfm 降频 3s → 10s
- 屏幕闪烁 max_brightness 适配
- security_check 记录退出原因
- Loading 超时提示 (5s 无响应)

## 性能优化
- inotify 安全检测快速通道
- 崩溃重启指数退避 (3s→6s→12s→max 60s)
- service.sh 锁文件防重复启动

## Bug 修复
- 修复 --sign 路径导致密钥验证失败
- 修复终端版本号硬编码
- 版本号统一 v6.1
- 移除 pkill 误杀
- 移除无效的 JS 完整性校验
- 回退 v6.0 的 watchdog/setpgid