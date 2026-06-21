# v6.8 更新内容
- 诊断: daemon 无响应时自动检测进程状态 + .pipe_ack + 日志
- 修复: exec_pipe() 关键路径移除 _S() 字符串加密, 防止 ARM64 崩溃
- 优化: daemon 收到 pipe 请求后写入 .pipe_ack 确认文件
