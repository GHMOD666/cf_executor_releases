# v6.7 更新内容

修复 daemon O_TRUNC 截断 WebUI 启动消息 → 改为 O_APPEND
修复终端输出混乱: 时序问题导致启动消息被 daemon 截断覆盖
daemon 超时/错误消息增加 T.innerHTML 直接写入作为兜底
WebUI 启动消息统一走 output.log 单一数据源