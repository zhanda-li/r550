# 项目约定

- 默认中文，事实与待确认信息分开记录；遵循用户全局 AGENTS.md 约定。
- ROS 工作空间、代码和仓库路径使用纯 ASCII；中文只用于文档。
- 不改 ~/.bashrc、/etc；不执行 rm -rf；推送和改写历史先征得用户同意。
- 优先单包构建：MAKEFLAGS=-j2，--parallel-workers 4。
- 本机无 NVIDIA GPU，CUDA/TensorRT 包空转属于预期；车载 Orin 另行确认。
- 原始厂商资料保留原位，不提交压缩包、固件、视频、模型、数据集和密钥。
- 顶配阿克曼刷固件前，必须备份本车舵机标定参数和现有配置，不能套用手册示例值。
- 进展写 PROGRESS.md；阶段总结写 docs/summaries/；提交后将 hash 追加到 PROGRESS.md。
- 完成修改后报告文件、验证、结果及未验证项。
