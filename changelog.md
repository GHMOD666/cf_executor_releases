# v6.12 更新内容
- 修复: pipe 文件写入改用 printf 直接写入路径, 不再依赖 base64/heredoc
- 修复: jj_key 文件也改用 printf 直接写入, 彻底解决 shell 管道兼容性问题
- 说明: Android toybox 的 base64 不支持 stdin pipe, heredoc 在 api.exec 单行传递中无法正常工作
