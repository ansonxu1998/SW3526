## SW3526

SW3526 是一款高集成度的多快充协议充电芯片，支持 C 口或A 口输出，其集成了3.5A高效率同步降压变换器，支持 PPS/PD/QC/AFC/FCP/SCP/PE/SFCP 等多种快充协议以及CC/CV模式。外围只需少量的器件，即可组成完整的高性能多快充协议充电解决方案。

### 同步降压变换器

+ 输出电流高达 3.5A
+ 输入电压范围 6~35V
+ 支持 CC/CV 模式
+ 支持线损补偿

### 快充协议

+ 支持 PPS/PD3.0/PD2.0
+ 支持 QC4+/QC4/QC3.0/QC2.0
+ 支持 AFC
+ 支持 FCP
+ 支持低压 SCP/高压 SCP
+ 支持 PE2.0/PE1.1
+ 支持 SFCP

### 保护机制

+ 软启动
+ 输入过压保护
+ 输入欠压保护
+ 输出过流保护
+ 输出短路保护
+ 过温保护

### 典型电路

![](/img/SW3526-1.png)

![](/img/SW3526-2.png)

## CH224K

CH224 单芯片集成 USB PD 等多种快充协议，支持 PD3.0/2.0，BC1.2 等升压快充协议，自动检测 VCONN 及模拟 E-Mark 芯片，最高支持 100W 功率，内置 PD 通讯模块，集成度高，外围精简。集成输出电 压检测功能，并且提供过温、过压保护等功能。

### 特点：

+ 支持 4V 至 22V 输入电压
+ 支持 PD3.0/2.0，BC1.2 等快充协议
+ 支持 USB Type-C PD，支持正反插检测与自动切换
+ 支持 E-Mark 模拟，自动检测 VCONN，支持 100W 功率的 PD 请求
+ 内置过压保护模块 OVA、超温保护模块 OTA

### 电压档位配置

#### 单电阻配置

CFG1 对 GND 连接电阻，不同阻值对应不同的电压请求档位。使用单电阻配置方式时，CFG2 和 CFG3 引脚 可悬空。电阻-请求电压对照表如下。

![](/img/CH224K-1.png)

#### 电平配置

CFG1，CFG2，CFG3直接连接到外部MCU的IO口，或直接连接CH224K/CH224D芯片的VDD/GND管脚，使用 电平对请求电压进行配置。真值表如下。

![](/img/CH224K-2.png)

### 典型电路

![](/img/CH224K-3.png)

## 原理图

![SCH_Schematic](/img/SCH_Schematic.png)

> 可以通过协议接口按照快充协议输出，也可以通过打开开关，使用 CH224K 芯片诱骗 SW3526 进行 PD 20V 输出。

## PCB

![3D_PCB](/img/3D_PCB.png)

![SW3526](/img/SW3526.jpg)

