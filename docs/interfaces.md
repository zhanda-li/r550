# ROS 2 接口核对表

以下为待核对的接口约定，不代表厂商实车已使用这些名称或类型。

| 链路 | 建议/候选接口 | 必须确认 |
| --- | --- | --- |
| 算法 → 底盘 | geometry_msgs/msg/Twist 或 ackermann_msgs/msg/AckermannDriveStamped | 实际 topic、类型、频率、速度单位、角速度还是转角、限幅与超时 |
| 底盘 → 里程计 | nav_msgs/msg/Odometry | topic、frame、单位、协方差、频率 |
| IMU → 状态估计 | sensor_msgs/msg/Imu | 来源、轴向、单位、时间戳、标定 |
| 雷达 → 感知 | sensor_msgs/msg/PointCloud2 | 型号、IP/端口、驱动、frame、频率、时间同步 |
| TF | map → odom → base_link → 传感器 | 各变换唯一发布者、外参、是否实际使用其他 frame 名称 |
| 电池/急停/使能 | 待查 | 消息来源、状态含义、恢复条件 |

阿克曼控制不能假定支持原地旋转；Twist 的 angular.z 含义及低速转向处理须对照驱动、固件和实测。检查多控制源仲裁，确认唯一有效控制源。
