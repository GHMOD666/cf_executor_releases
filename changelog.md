# v6.16 更新内容
- 修复: 大退重进后密钥和自定义路径丢失 (KernelSU WebUI 清除 localStorage)
- 修复: 初始化时 selectScript 不再清除卡密状态
- 修复: pipe 写入检查竞态条件 (daemon 可能先于 WebUI 删除 pipe 文件)
- 新增: 文件持久化双保险机制, 关键设置同步到 /sdcard/cf_executor/.settings
- 新增: 30秒定时同步 localStorage 到文件, 2.5秒后从文件恢复缺失设置
- 优化: selectScript 增加 fromInit 参数, 区分初始加载和用户操作
