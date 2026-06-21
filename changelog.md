# v6.10 更新内容
- 修复: pipe 文件写入改用 printf 替代 echo, 防止 base64 特殊字符被 shell 转义
- 诊断: pipe 写入后立即验证文件大小, 写入失败时尝试备用方式
- 诊断: exec_pipe 读到空文件时记录 pipe: empty or read fail 日志
- 增强: 超时诊断增加 pipe_exec 文件存在性检查, 区分未处理/空文件/ACK 三种情况
- 修复: jj_key 文件也改用 printf 写入
