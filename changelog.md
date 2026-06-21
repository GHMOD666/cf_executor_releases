# v7.3 更新内容
- 修复: 脚本选项点不动 (warnModal 关闭不彻底导致遮罩残留)
- 修复: closeWarnModal 强制 style.display=none, 确保遮罩完全移除
- 修复: 显示 warnModal 时强制 style.display=flex, 防止 CSS 优先级问题
- 优化: .opt 选项增加 position:relative+z-index:1+pointer-events:auto, 确保可点击
