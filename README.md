# 25edc
This is a platform for my teammates and me to manage our study and preparation plan to National Undergraduate Electronics Design Contest and record the process.

## 备赛方向：控制类（主），XXX（副）
### 所需技术栈：
- **硬件：**
  - **pcb绘制**
  - **器件选型：**
    - 输入外设：测距（超声波），角度（陀螺仪），图像（k210），循迹（红外，灰度），速度（编码器），交互（按键）
    - 输出外设：
      - 运动控制：电机驱动模块（TB6612，L298N），电机（直流电机，步进电机，舵机）
      - 交互：OLED屏幕，LED指示灯，蜂鸣器
    - 通信：蓝牙模块（CH-05），wifi
- **软件：**
  - **驱动：** 定时器，中断，外设驱动
  - **算法：** pid控制算法，信号处理（图像处理，滤波）
  - **功能：** 循迹，识别（色块，数字），目标定位寻踪，测距，人机交互
- **报告文档：**
  - 公式，图标，测试数据
### 所需工具：
- 硬件材料：
- 工具：螺丝刀，螺丝螺母螺柱，电烙铁热风枪，锡丝锡膏
- 软件：Keil5，STM32CubeMX，STM32CubeIDE，canmvIDE
  
