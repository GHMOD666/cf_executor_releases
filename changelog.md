# v6.17 更新内容
- 新增: WebUI 版本更新检测, 启动时自动抓取 update.json 并与本地版本对比
- 新增: 更新横幅 (绿色), 点击跳转下载, 可手动关闭
- 新增: ptrace 自附着防调试 (PTRACE_TRACEME), 阻止外部调试器附加
- 新增: /proc/self/maps 运行时哈希校验, 每30秒比较, 检测到注入立即退出
- 新增: mprotect 反内存 dump 保护, 验证内存保护机制可用性
- 优化: 周期性安全检测跳过 ptrace 自附着 (仅首次有效), 避免误报
- 安全: 新增 sec:ptrace occupied 和 sec:maps changed 日志记录
