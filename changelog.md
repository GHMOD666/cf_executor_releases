# v8.0 更新内容
- 重大修复: 持久化存储重构, 解决 KernelSU WebView 大退后 localStorage 丢失问题
- 原理: 所有设置(卡密/记住密码/自定义路径/主题/亮度/脚本模式/环境/Tab)同时写入 /sdcard/cf_executor/.webui_state 文件
- 原理: 页面加载后从文件恢复状态, 覆盖 localStorage 的默认值
- 原理: 300ms 防抖批量写入, 减少 I/O 开销
- 影响: 大退重进后卡密保留、自定义路径保留、所有设置保留
