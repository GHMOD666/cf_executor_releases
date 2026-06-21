# v6.13 更新内容
- 修复: pipe 文件写入改用 echo 替代 printf, api.exec 底层会将 % 转义导致 printf 输出空字符串
- 修复: jj_key 文件也改用 echo 写入
- 确认: daemon 正常运行 (v6.12 日志证实已进入 listening 状态并收到 pipe 文件)
- 确认: 问题定位为 pipe 文件内容为空, 非 daemon 崩溃
