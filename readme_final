# EFI for Sony VAIO SVF15A18SCB - macOS Catalina 10.15.7

## 🖥️ 硬件配置 | Hardware Configuration

| 组件 | 型号 | 状态 |
|------|------|------|
| **CPU** | Intel Core i5-3337U (Ivy Bridge) | ✅ 正常工作 |
| **集成显卡** | Intel HD Graphics 4000 | ✅ 已驱动 |
| **主板芯片组** | Intel HM76 | ✅ 正常工作 |
| **无线网卡** | Intel AC 8265 PCIe | ✅ 已驱动 |
| **蓝牙** | Intel AC 8265 (USB) | ✅ 已驱动 |
| **存储** | SATA SSD | ✅ 正常工作 |
| **触摸屏** | 单点触控 (USB) | ✅ 已驱动 |
| **触摸板** | SMBus 协议 | ✅ 已驱动 |
| **有线网卡** | Realtek RTL8111 | ✅ 已驱动 |
| **读卡器** | Realtek Card Reader | ✅ 已驱动 |
| **独显** | NVIDIA GT 740M | ❌ 已屏蔽 |

## 📋 功能状态 | Features Status

### ✅ 正常工作 | Working Features
- 系统启动 | System Boot
- 显卡加速 (HD 4000) | Graphics Acceleration
- 无线网络 (Intel 8265) | Wi-Fi
- 蓝牙 | Bluetooth
- 触摸板 (VoodooPS2 + VoodooSMBus) | TouchPad
- 触摸屏 (VoodooI2C) | Touch Screen
- USB 3.0 & 2.0
- 键盘及快捷键 | Keyboard & Brightness Keys
- 音频 (layout-id: 27) | Audio
- 电源管理 | Power Management
- 电池状态 | Battery Status
- 有线网络 | Ethernet
- SD卡读卡器 | SD Card Reader

### ❌ 不正常工作 | Not Working
- **AirDrop** - Intel网卡不支持原生AirDrop
- **NVIDIA 独立显卡** - 已通过SSDT屏蔽

### ⚠️ 部分工作 | Partially Working
- 隔空播放 | AirPlay (有限支持)
- 接力 | Handoff (有限支持)

## 🚀 快速开始 | Quick Start


### 1. 必要配置步骤 | Required Configuration Steps

#### 1.1 重新生成 PlatformInfo
发布版本已清空序列号，请根据OpenCore官方指南重新生成：
```bash
# 使用GenSMBIOS工具生成
# 或使用ProperTree/OpenCore Configurator
```

#### 1.2 显卡配置
- DeviceProperties → AAPL,ig-platform-id: `0600260A`
- 已配置帧缓冲补丁

#### 1.3 音频配置
当前使用引导参数：`alcid=27`

### 3. 内核扩展说明 | Kernel Extensions Details

#### 3.1 必需驱动 | Required Drivers
| 驱动名称 | 版本 | 功能 |
|----------|------|------|
| **Lilu.kext** | 最新版 | 基础补丁框架 |
| **VirtualSMC.kext** | 最新版 | SMC模拟 |
| **WhateverGreen.kext** | 最新版 | 显卡修复 |
| **AppleALC.kext** | 1.7.8+ | 音频驱动 (使用AppleALCU.kext替代) |
| **VoodooPS2Controller.kext** | 最新版 | PS2输入设备 |
| **VoodooSMBus.kext** | 最新版 | SMBus触摸板 |

#### 3.2 无线和蓝牙 | Wi-Fi & Bluetooth
| 驱动名称 | 功能 | 备注 |
|----------|------|------|
| **AirportItlwm.kext** | Intel无线驱动 | Catalina专用版 |
| **itlwm.kext** | Intel无线驱动 | 备用 |
| **IntelBluetoothFirmware.kext** | 蓝牙固件 | |
| **IntelBluetoothInjector.kext** | 蓝牙注入 | |
| **IntelBTPatcher.kext** | 蓝牙补丁 | 可选 |

#### 3.3 触摸屏和I2C | Touch Screen & I2C
| 驱动名称 | 功能 |
|----------|------|
| **VoodooI2C.kext** | I2C总线驱动 |
| **VoodooI2CHID.kext** | HID触摸设备 |
| **VoodooI2CELAN.kext** | ELAN触摸屏 |
| **VoodooI2CSynaptics.kext** | Synaptics触摸屏 |
| **VoodooI2CFTE.kext** | FTE触摸屏 |
| **VoodooI2CAtmelMXT.kext** | Atmel触摸屏 |
| **VoodooRMI.kext** | RMI协议支持 |
| **VoodooInput.kext** | 输入框架 |

#### 3.4 其他硬件 | Other Hardware
| 驱动名称 | 功能 |
|----------|------|
| **RealtekRTL8111.kext** | 有线网卡 |
| **RealtekCardReader.kext** | SD卡读卡器 |
| **SMCBatteryManager.kext** | 电池管理 |
| **SMCProcessor.kext** | 处理器监控 |
| **SMCSuperIO.kext** | Super I/O监控 |

#### 3.5 实用工具 | Utilities
| 驱动名称 | 功能 |
|----------|------|
| **ECEnabler.kext** | 嵌入式控制器 |
| **BrightnessKeys.kext** | 亮度快捷键 |
| **DebugEnhancer.kext** | 调试增强 |

## ⚠️ 重要提醒 | Important Notes

### 关于AirDrop支持
**Intel无线网卡不支持原生AirDrop功能**。如需完整Continuity功能：
1. **更换网卡**为Broadcom系列：
2. **使用第三方工具**：部分第三方应用可模拟AirDrop功能

### 关于版本选择
- **OpenCore**: 建议使用 0.9.0+ 版本
- **macOS**: 本EFI针对Catalina 10.15.7优化
- **驱动版本**: 请保持所有驱动最新

### 关于版权声明
```
本项目使用了大量开源社区资源，所有权利归原开发者所有。
如果任何资源侵犯了您的版权，请联系：qaqmolingqaq@qaqmolingqaq.top
我们将立即处理。
```

## 🔄 更新日志 | Changelog

### v1.06 (当前版本)
- 更新所有驱动至最新版本
- 优化触摸屏驱动配置
- 改进电源管理
- 修复睡眠/唤醒问题
- 完善USB端口映射

### v1.05 (旧版本)
- 基础功能实现
- 初版EFI发布
- 部分配置不完整

## 📞 支持与联系 | Support & Contact

### 问题反馈
1. **GitHub Issues**: 提交具体问题
2. **Email**: qaqmolingqaq@qaqmolingqaq.top

### 需要提供的信息
```markdown
1. 问题描述
2. 系统日志 (使用 `log show --last boot`)
3. 硬件详细信息
4. 已尝试的解决方案
```

## 📄 许可证 | License

本项目基于多个开源项目构建，各自遵循其原始许可证。
配置文件和文档部分采用 [MIT License](LICENSE)。

```
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

**最后更新**: 2026-01-31  
**适用系统**: macOS Catalina 10.15.7  
**测试机型**: Sony VAIO SVF15A18SCB  
**维护者**: QAQmolingQAQ

> **注意**: 使用前请务必备份原始EFI和个人数据！
