# RoboParty 61 仓索引

[RoboParty](https://github.com/Roboparty)（上海萝博派对）全部 **61 个公开仓库**的学习索引。整理目的：人形机器人自研过程中，参考其结构思路、电机选型逻辑与开发流程。

## 三个入口

| 入口 | 内容 |
| --- | --- |
| **[我的 61 个 fork](https://github.com/4dr2k5h66m-collab?tab=repositories)** | 源码本体，与上游逐字节一致，未做修改、未重新打包 |
| **[全量盘点报告（33 页）](./RoboParty开源仓库全量文件盘点与自研借鉴评估报告.docx)** | 61 仓的总体规模、分类、图纸与 PCB 分布、许可分档、自研借鉴评估 |
| **[docs/ 单仓说明（61 册）](./docs/)** | 一个仓库一册：概况、顶层条目索引、逐目录用途说明、完整文件清单 |

## 查阅地图：你要看什么 → 进哪个仓

| 你要看的东西 | 仓库 | 里面是什么 |
| --- | --- | --- |
| 机械图纸 · PCB · BOM | `rpo_hardware` | V1.0 / V2.0 两代：机械总装、PCB、制造文件、URDF；176 个 .sldprt、187 个 STEP/STP、64 个 STL、28 张工程图，同名 STEP 与 PDF 都配好了 |
| 整机三维总装 | `roboto_origin` | 整机总装配体；自身仅 27 个文件，另以子模块方式挂了 8 个模块 |
| 外观件 · 外壳 | `rpo_appearance` | V1.0 下 53 个中文命名 STL |
| 运动学模型 | `rpo_description` | urdf/rpo.urdf、mjcf/rpo.xml 加 24 个 STL，可直接喂 Gazebo / MuJoCo |
| 电机选型 | `roboparty_motors` | 四家电机驱动（dm / evo / lro / xyn） |
| 灵巧手 | `roboparty_dexhand` 等 3 个 | RP_Hand 6 DOF、CAN-FD，附 ROS2 控制与骨骼遥操作 |
| 传感器 | `roboparty_imu`、`roboparty_camera`、`roboparty_lidar` | IMU（hipnuc + MD7123 双驱动）、相机、雷达 |
| 电池 · 充电 | `roboparty_bms`、`roboparty_charger` | LB-13S2P 电池；STM32F103 充电器，Type-C PD 最高 140 W |
| 固件 | `roboparty_firmware` 等 3 个 | 嵌入式固件与 USB-CAN 工具 |
| 部署 · 推理 | `roboparty_deploy` 等 3 个 | Orange Pi 5 Plus / RDK X5 部署；9 个 ONNX 策略 |
| 训练 · 仿真 | `roboparty_train` 等 4 个 | 强化学习训练与仿真环境 |
| 遥操作 · 数据采集 | `roboparty_xr_teleop` 等 4 个 | XR 遥操作、数据采集 |
| 下一代机型线索 | `roboparty_teleop_wam`、`roboparty_dexhand` | configs 暴露 RP1 / 28 DoF；总线迁往 EtherCAT 的痕迹在 `roboparty_build` 与 `igh-deb` |

## 图纸与 PCB 的具体位置

全在 `rpo_hardware`（647 个文件）：

- `V1.0/atom01_mechanic/` — 00_Docs、01_SW_Project、02_Manufacturing、03_URDF
- `V1.0/atom01_pcb/`
- `V2.0/roboto_origin_mechanic/`
- `V2.0/roboto_origin_pcb/`（含 OPI-5PLUS-PCBA 的 .stp 与 .SLDPRT）

不用装 SolidWorks 也能看：`.sldprt` 基本都配了同名 `.step` 导出，工程图都配了同名 PDF。

## 61 个仓库清单

| 仓库 | 源码（fork） | 单仓说明 |
| --- | --- | --- |
| `.github` | [源码](https://github.com/4dr2k5h66m-collab/.github) | [文档](./docs/.github.docx) |
| `ACoT-VLA` | [源码](https://github.com/4dr2k5h66m-collab/ACoT-VLA) | [文档](./docs/ACoT-VLA.docx) |
| `Bi_PiPER_with_DexHand` | [源码](https://github.com/4dr2k5h66m-collab/Bi_PiPER_with_DexHand) | [文档](./docs/Bi_PiPER_with_DexHand.docx) |
| `GMR` | [源码](https://github.com/4dr2k5h66m-collab/GMR) | [文档](./docs/GMR.docx) |
| `GR00T-WholeBodyControl_unitree` | [源码](https://github.com/4dr2k5h66m-collab/GR00T-WholeBodyControl_unitree) | [文档](./docs/GR00T-WholeBodyControl_unitree.docx) |
| `INTACT-JEPA` | [源码](https://github.com/4dr2k5h66m-collab/INTACT-JEPA) | [文档](./docs/INTACT-JEPA.docx) |
| `LabWeft` | [源码](https://github.com/4dr2k5h66m-collab/LabWeft) | [文档](./docs/LabWeft.docx) |
| `MimicLite` | [源码](https://github.com/4dr2k5h66m-collab/MimicLite) | [文档](./docs/MimicLite.docx) |
| `P-BFM` | [源码](https://github.com/4dr2k5h66m-collab/P-BFM) | [文档](./docs/P-BFM.docx) |
| `Party_OS` | [源码](https://github.com/4dr2k5h66m-collab/Party_OS) | [文档](./docs/Party_OS.docx) |
| `SOEM` | [源码](https://github.com/4dr2k5h66m-collab/SOEM) | [文档](./docs/SOEM.docx) |
| `UFO` | [源码](https://github.com/4dr2k5h66m-collab/UFO) | [文档](./docs/UFO.docx) |
| `create_ap` | [源码](https://github.com/4dr2k5h66m-collab/create_ap) | [文档](./docs/create_ap.docx) |
| `dm_pd_optimizer` | [源码](https://github.com/4dr2k5h66m-collab/dm_pd_optimizer) | [文档](./docs/dm_pd_optimizer.docx) |
| `firmware` | [源码](https://github.com/4dr2k5h66m-collab/firmware) | [文档](./docs/firmware.docx) |
| `gpt-6-astra-real2sim-workflow` | [源码](https://github.com/4dr2k5h66m-collab/gpt-6-astra-real2sim-workflow) | [文档](./docs/gpt-6-astra-real2sim-workflow.docx) |
| `human-humanoid-tools` | [源码](https://github.com/4dr2k5h66m-collab/human-humanoid-tools) | [文档](./docs/human-humanoid-tools.docx) |
| `igh-deb` | [源码](https://github.com/4dr2k5h66m-collab/igh-deb) | [文档](./docs/igh-deb.docx) |
| `legged_lab` | [源码](https://github.com/4dr2k5h66m-collab/legged_lab) | [文档](./docs/legged_lab.docx) |
| `robolab` | [源码](https://github.com/4dr2k5h66m-collab/robolab) | [文档](./docs/robolab.docx) |
| `roboparty_all` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_all) | [文档](./docs/roboparty_all.docx) |
| `roboparty_base` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_base) | [文档](./docs/roboparty_base.docx) |
| `roboparty_bms` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_bms) | [文档](./docs/roboparty_bms.docx) |
| `roboparty_build` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_build) | [文档](./docs/roboparty_build.docx) |
| `roboparty_camera` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_camera) | [文档](./docs/roboparty_camera.docx) |
| `roboparty_capture` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_capture) | [文档](./docs/roboparty_capture.docx) |
| `roboparty_charger` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_charger) | [文档](./docs/roboparty_charger.docx) |
| `roboparty_deb_template` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_deb_template) | [文档](./docs/roboparty_deb_template.docx) |
| `roboparty_deploy` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_deploy) | [文档](./docs/roboparty_deploy.docx) |
| `roboparty_description` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_description) | [文档](./docs/roboparty_description.docx) |
| `roboparty_dexhand` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_dexhand) | [文档](./docs/roboparty_dexhand.docx) |
| `roboparty_dexhand_ros` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_dexhand_ros) | [文档](./docs/roboparty_dexhand_ros.docx) |
| `roboparty_dexhand_teleop` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_dexhand_teleop) | [文档](./docs/roboparty_dexhand_teleop.docx) |
| `roboparty_example` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_example) | [文档](./docs/roboparty_example.docx) |
| `roboparty_firmware` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_firmware) | [文档](./docs/roboparty_firmware.docx) |
| `roboparty_image` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_image) | [文档](./docs/roboparty_image.docx) |
| `roboparty_imu` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_imu) | [文档](./docs/roboparty_imu.docx) |
| `roboparty_inference` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_inference) | [文档](./docs/roboparty_inference.docx) |
| `roboparty_lidar` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_lidar) | [文档](./docs/roboparty_lidar.docx) |
| `roboparty_motors` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_motors) | [文档](./docs/roboparty_motors.docx) |
| `roboparty_navigation` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_navigation) | [文档](./docs/roboparty_navigation.docx) |
| `roboparty_onnxruntime` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_onnxruntime) | [文档](./docs/roboparty_onnxruntime.docx) |
| `roboparty_rdk` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_rdk) | [文档](./docs/roboparty_rdk.docx) |
| `roboparty_repo` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_repo) | [文档](./docs/roboparty_repo.docx) |
| `roboparty_rp_head` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_rp_head) | [文档](./docs/roboparty_rp_head.docx) |
| `roboparty_rp_server` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_rp_server) | [文档](./docs/roboparty_rp_server.docx) |
| `roboparty_start` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_start) | [文档](./docs/roboparty_start.docx) |
| `roboparty_stm32_usbcan` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_stm32_usbcan) | [文档](./docs/roboparty_stm32_usbcan.docx) |
| `roboparty_teleop_wam` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_teleop_wam) | [文档](./docs/roboparty_teleop_wam.docx) |
| `roboparty_train` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_train) | [文档](./docs/roboparty_train.docx) |
| `roboparty_xr_teleop` | [源码](https://github.com/4dr2k5h66m-collab/roboparty_xr_teleop) | [文档](./docs/roboparty_xr_teleop.docx) |
| `robopi_addon` | [源码](https://github.com/4dr2k5h66m-collab/robopi_addon) | [文档](./docs/robopi_addon.docx) |
| `robopi_analyze` | [源码](https://github.com/4dr2k5h66m-collab/robopi_analyze) | [文档](./docs/robopi_analyze.docx) |
| `robopi_config` | [源码](https://github.com/4dr2k5h66m-collab/robopi_config) | [文档](./docs/robopi_config.docx) |
| `robopi_firmware` | [源码](https://github.com/4dr2k5h66m-collab/robopi_firmware) | [文档](./docs/robopi_firmware.docx) |
| `roboto_origin` | [源码](https://github.com/4dr2k5h66m-collab/roboto_origin) | [文档](./docs/roboto_origin.docx) |
| `rpo_appearance` | [源码](https://github.com/4dr2k5h66m-collab/rpo_appearance) | [文档](./docs/rpo_appearance.docx) |
| `rpo_description` | [源码](https://github.com/4dr2k5h66m-collab/rpo_description) | [文档](./docs/rpo_description.docx) |
| `rpo_hardware` | [源码](https://github.com/4dr2k5h66m-collab/rpo_hardware) | [文档](./docs/rpo_hardware.docx) |
| `rsl_rl` | [源码](https://github.com/4dr2k5h66m-collab/rsl_rl) | [文档](./docs/rsl_rl.docx) |
| `soem-deb` | [源码](https://github.com/4dr2k5h66m-collab/soem-deb) | [文档](./docs/soem-deb.docx) |

## 授权与使用边界（重要）

61 个仓库的许可并不统一：

| 档位 | 数量 | 说明 |
| --- | --- | --- |
| 宽松型（MIT / Apache-2.0 / BSD） | 10 | 署名即可 |
| 传染型（GPL-2.0 / GPL-3.0） | 34 | 派生作品须以同一许可开放 |
| 硬件弱互惠（CERN-OHL-W-2.0） | 3 | 改了机械设计并对外提供产品时，修改版设计文件须以同一许可开放 |
| 许可状态不明（NOASSERTION） | 4 | 未识别到标准许可 |
| 无许可证（默认保留所有权利） | 10 | 未声明许可 |

这些仓库在这里**只作为学习资料**。把图纸、PCB、URDF 或源码直接拿来做自己的产品，存在明确的许可风险，GPL 系列与 CERN-OHL-W 尤其带传染条款。所有源码以 fork 形式保留在原仓库、未做修改也未重新打包上传，随时可与上游同步。

## 数据口径

- 61 个仓库，28,262 个受控文件，5,607 个目录
- 全量盘点报告：33 页，含 5 张表、3 张图
- 单仓说明：61 册，文件名与仓库名逐字符一致，位于 `docs/`
- 索引整理时间：2026-10-05
