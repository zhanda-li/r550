# R550 越野感执一体软件项目

负责范围：传感器调试、电机控制、ROS 2 接口对齐及后续算法实车部署。

## 路径与硬件

- 软件仓库及 ROS 工作空间：`/home/lizhanda/r550`、`/home/lizhanda/r550/ros2_ws`（纯 ASCII）。
- 原始资料：`/home/lizhanda/越野感执一体/R550资料`，外置保留，不纳入 Git。
- 用户提供配置：阿克曼 ROS 2 小车，R550 顶配独立悬挂重载型，Orin NX 8GB，镭神 32 线雷达。具体雷达型号、主控版本及车载系统待核实。
- 本机 Ubuntu 22.04 / ROS 2 Humble，无 NVIDIA GPU；车载 Orin 环境单独核实。

## 项目文档

- [资料初读与证据](docs/summaries/W-01_R550资料初读.md)
- [调试与验收顺序](docs/bringup.md)
- [接口核对表](docs/interfaces.md)
- [原始资料清单与 SHA-256](docs/vendor_manifest.json)
- [进展记录](PROGRESS.md)

当前仅建立文档和目录结构，未导入厂商 ROS 驱动，也未连接实车。
后续拿到车载现有工作空间后，先备份、确认版本，再按包接入。

有实际 ROS 包后，在 `ros2_ws` 中优先单包编译：

```bash
source /opt/ros/humble/setup.bash
MAKEFLAGS=-j2 colcon build --packages-select <package_name> --parallel-workers 4
```
