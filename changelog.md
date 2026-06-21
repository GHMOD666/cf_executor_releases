# v6.9 更新内容
- 崩溃诊断: 添加 SIGSEGV/SIGABRT 等信号处理器, 崩溃时记录信号+地址到 daemon.log
- 调试: main() 和 daemon_mode() 启动路径每步写入 raw_log, 精确追踪崩溃位置
- 修复: WebUI 超时诊断改为独立计时器, 不再依赖 api.exec promise 回调
- 增强: 诊断输出改为 tail -10 daemon.log, 显示更多上下文
