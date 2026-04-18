# 末端执行器信息提取

## 图像描述（末端执行器）

从图中可见，橙色多关节工业机器人手腕端连接了一个**吸附类末端执行器（真空吸盘夹具）**，朝向左侧工位的黑色条状/板状工件区域进行取放。

- **类型**：真空吸附式末端执行器（推断为多吸盘或吸附夹具）
- **可见组件**：
  - 与机器人腕部连接的安装板/转接座
  - 末端吸附接触面（吸盘阵列或吸附块）
  - 局部支架结构（用于固定吸附模块）
- **安装朝向**：安装于机器人法兰末端，姿态为向左下方工位方向伸出，接触面朝向待搬运工件
- **近似功能**：对条状/板状工件执行吸取、搬运、上下料（Pick-and-Place）

## 图片

![工业机器人末端执行器（吸附夹具）在产线工位执行取放作业](./assets/images/end-effector-source.jpg)

## 结构化输出（JSON）

```json
{
  "endEffectorType": "Vacuum suction gripper (multi-point suction, inferred)",
  "actuation": "Pneumatic vacuum (inferred from suction-style contact interface)",
  "contactInterface": "Flat/compliant suction contact pads or suction cup array",
  "visibleComponents": [
    "Wrist mounting adapter plate",
    "End-effector body/bracket",
    "Suction contact module"
  ],
  "mountingOrientation": "Mounted on robot wrist flange, tool face oriented toward left-side workstation and slightly downward",
  "approximateSizeCues": {
    "relativeToRobotWrist": "Tool head width appears roughly 1.2x-1.8x wrist diameter",
    "relativeToWorkpiece": "Contact span appears sized for single strip/plate pickup per cycle",
    "confidence": "low-to-medium (single image, partial occlusion)"
  },
  "mountingFlange": "Standard industrial robot wrist flange with adapter (exact standard not legible)",
  "cablesOrHosesVisibility": "Partially visible or occluded; vacuum lines likely present but not clearly resolved",
  "intendedOperation": "Automated pick-and-place/loading-unloading of elongated dark workpieces on a production line"
}
```
