# NUEDC--TRAINING
This is a platform for my teammates and me to manage our study and preparation plan to National Undergraduate Electronics Design Contest and record the process.

## 成员简介
| 成员名称 | 技术栈 | 职责 |
| -------- | ---------| -------- |
| A | 标准库，hal库开发STM32，C语言基础 | 团队协调和软件 |
| B | 
| C | 标准库开发STM32，C语言基础 | 软件 |
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
## 题目选择：智能送药小车
### 题目要求：
- **题目分析：**
  - **场景：** 1-8号房间模拟场地自动送药并返回
  - **流程：**
    - 装载：识别病房号（数字识别），手动装载药品
    - 运送：沿走廊中线循迹至目标病房（红色），在指定区域停止
    - 卸载与返回：指示灯指示，手动卸载，自动返回
  - **题目难点：**
    - ​**动态路径规划：** 病房位置（3-8号）随机设定，需实时识别并调整路径
    - ​**多车协同：** 双车需避免碰撞，通过无线通信同步状态，优化任务时序（优先完成基本要求）
​    - **时间限制：** 保证车速的同时准确地完成循迹和识别
​    - **数字识别：** 训练数字识别模型
  - **所需技术栈分析：**
    - 硬件
   

    | 模块 | 技术选型 | 分析 |
    |--------|--------|--------|
    | 主控芯片 | STM32主控 |
    | 循迹模块 | 红外对管（tcrt5000）或灰度传感器 | 红黑线扫描和循迹 |
    | 数字识别模块 | k210视觉模块 | 识别病房数字 |
    | 电机驱动 | TB6612，L298N | 驱动电机，PWM调速 |
    | 通信 | HC-05 | 同步指令 |
    | 状态检测 | 压力传感器或光电传感器 | 检测药物的装配和卸载 |
    | 电源控制 | 12V锂电池，LM2596稳压模块 | 12V转5V转3.3V |

    - 软件
   

    | 模块 | 技术方案 | 分析 |
    |-------|--------|--------|
    | 循迹控制 | PID算法 | 优化循迹路线 |
    | 数字识别 | k210数字识别模型 | 识别判断目标病房 |
    | 电机闭环控制 | PID算法 | 编码器测速，调整电机速度 |
    | 多任务协调 | 状态机，定时器配置 | 优化代码流程，防止时序错误 |

## 学习计划
- **提交方式：**
  - 硬件：使用嘉立创团队协作，将pcb原理图及实物图截图提交
  - 软件：将工程文件进行提交
  - 实物展示及功能完成通过视频提交
- **具体内容：**
- **第一周** （3.17-3.23）
  - 题目分析，完成器件选型，和开发流程
  - 搭建一个基本软硬件框架（基础小车搭建，完成基本功能代码的编写）
- **第二周** （3.24-3.30）
  - 完成pcb绘制打板焊接测试
  - 完成基本要求1，2
- **第三周** （3.31-4.6）
  - pcb调整和优化（如果存在较大问题）
  - 完成基本要求3
- **第四周** （4.7-4.13）
  - 进行全任务整体测试调整





