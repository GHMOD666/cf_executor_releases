# v6.5 更新内容

修复终端空白/卡住问题: pollOnce 截断检测 + triggerCmd 先清空 output.log
修复 T.textContent/T.innerHTML 不一致导致启动消息被覆盖
pollOnce/writeToPipe 增加文件截断检测, 自动重置 lastLogLen