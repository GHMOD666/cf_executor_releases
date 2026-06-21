# v8.4 更新内容
- 安全: /proc/pid/exe 伪装, daemon 启动后 mount --bind /system/bin/sh 覆盖自身二进制
- 效果: ls -l /proc/pid/exe 仍显示原始路径, 但二进制内容已是 sh, file 命令无法识别
- 效果: 结合 prctl(PR_SET_NAME, "sh"), 双重伪装, ps/top 显示为 sh 进程
- 注意: service.sh 重启前会 umount -l 卸载伪装, 确保 daemon 正常启动
