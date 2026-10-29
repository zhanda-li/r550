# 项目进展

## 2026-10-29 · 项目初始化

- 动作：盘点 R550资料，pdftotext 提取关键 PDF；只读检查默认 STM32 压缩包部分源码；建立纯 ASCII 仓库 `/home/lizhanda/r550`。
- 结果：形成资料初读、接口核对表、调试顺序和带 SHA-256 的 177 文件清单；原始资料未移动或修改。
- 证据：docs/summaries/W-01_R550资料初读.md、docs/vendor_manifest.json。
- 验证：文档相对链接检查通过；资料清单 177 项计数一致；仓库路径为 ASCII；git check-ignore 确认 ROS 产物、数据、.env 和本地配置被忽略。
- 遗留：未连接实车、未构建 ROS 包、未验证雷达/底盘通信；随货手册图文未逐页查看。
