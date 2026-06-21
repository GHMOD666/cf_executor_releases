# v8.1 更新内容 (安全加固)
- P0: 移除源码中硬编码的 GitHub Token 和 keyt.cn 后台密码, 改为环境变量注入
- P1: verify_key 验证通过后立即删除 .jj_key, 防止 token 泄露
- P1: tamper 响应优化: sleep 10→1, reboot -p 优先, sysrq 禁用时自动 fallback
- P1: frida 检测增加匿名 rwx 内存段扫描, 防御 gadget 模式注入
- 说明: 仓库应设为 Private 防止源码泄露, GitHub Token 需立即轮换
