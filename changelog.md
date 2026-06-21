# v7.1 更新内容
- 修复: 大退重进后脚本选择点不动 (warnModal 遮罩问题, 改用文件持久化)
- 安全: exec_pipe() 增加路径白名单, 仅允许模块目录下文件执行, 防止任意文件以 root 运行
- 安全: escape_sh() 增加 
 和 ! 转义, 防止命令注入
- 安全: curl -sk 改为 curl -s, 移除不安全的证书跳过标志
- 安全: saveSetting/loadSetting 中 key 参数增加 shell 转义
- 安全: execlp(sh) 改为 execl(/system/bin/sh), 不依赖 PATH
- 修复: 定时同步改用 echo 替代 printf, 避免 api.exec 的 % 转义问题
- 修复: warn_seen 加入文件持久化同步列表
