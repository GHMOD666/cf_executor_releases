# v6.11 更新内容
- 修复: pipe 文件写入改用 heredoc (cat << 'EOF'), 彻底绕过 base64 命令兼容性问题
- 修复: jj_key 文件也改用 heredoc 写入, 不再依赖 base64
- 修复: update.json 下载链接改用 raw.githubusercontent.com, 避免 GitHub Pages 404
