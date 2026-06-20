# v6.6 更新内容

重构终端输出架构: 所有消息统一走 output.log 单一数据源
pollOnce 截断时替换而非追加, 消除旧内容残留
WebUI 启动消息通过 echo 写入 output.log, 不再直接写 T.innerHTML
修复 daemon O_TRUNC 导致终端内容混乱的问题