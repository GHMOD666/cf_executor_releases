# CF Executor v6.3

🔧 修复 daemon 崩溃 (dprintf + _S() 不兼容 → write())
🔧 output.log 初始化移到最前面 (防崩溃时日志丢失)
📋 版本号 v6.3