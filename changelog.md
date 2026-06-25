# v10.3 更新内容

- 崩溃处理器重写 (仅 async-signal-safe 函数, 无 localtime/snprintf)
- 反调试加固: ptrace 自追踪占位 + 安全检测窗口缩短至 10s + 二进制内容哈希校验
- 修复所有 TOCTOU 竞态条件 (access→open+fstat 原子化)
- daemonVerify 合并模式行数兜底
- 清除死代码: 移除冗余 waitpid/未使用变量/不可达代码
