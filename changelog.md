# CF Executor v6.1

🔧 回退 watchdog/setpgid (v6.0 引入的 bug 导致脚本卡死)
🔧 超时改用主循环轮询 (读 .pipe_start_ts, 300s 自动 kill)
🔧 service.sh 锁文件 + 旧 daemon 终止等待 3s
📋 版本号 v6.1