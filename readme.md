# EFI for Sony VAIO SVF15A18SCB - macOS Catalina 10.15.7

## 🖥️ 硬件配置 | Hardware Configuration

| 组件 | 型号 | 状态 |
|------|------|------|
| **CPU** | Intel Core i5-3337U (Ivy Bridge) | ✅ 正常工作 |
| **集成显卡** | Intel HD Graphics 4000 | ✅ 已驱动 |
| **主板芯片组** | Intel HM76 |  |
| **无线网卡** | Intel AC 8265 PCIe | ✅ 已驱动 |
| **蓝牙** | Intel AC 8265 (USB) | ✅ 已驱动 |
| **存储** | SATA SSD | ✅ 正常工作 |
| **触摸屏** |  USB | ✅ 已驱动 |
| **触摸板** | SMBus 协议 | ✅ 已驱动 |
| **有线网卡** | Realtek RTL8111 | ✅ 已驱动 |
| **读卡器** | Realtek Card Reader | ✅ 已驱动 |
| **独显** | NVIDIA GT 735M | ❌ 已屏蔽 |

## 📋 功能状态 | Features Status

### ✅ 正常工作 | Working Features
- 系统启动 | System Boot
- 显卡加速 (HD 4000) | Graphics Acceleration
- 无线网络 (Intel ac 8265) | Wi-Fi
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
- **NVIDIA 独立显卡** - 已屏蔽

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


## 🙏 致谢 | Credits

本项目的成功得益于众多优秀的开源项目与开发者。在此，我们向所有为 Hackintosh 社区做出贡献的人们表示最诚挚的感谢。

### 🛠️ 核心项目 | Core Projects
以下项目是本 EFI 得以运行的基石：
| 项目 | 
| :--- | 
| [**OpenCore**](https://github.com/acidanthera/OpenCorePkg) |
| [**Lilu**](https://github.com/acidanthera/Lilu) | **Acidanthera** |
| [**WhateverGreen**](https://github.com/acidanthera/WhateverGreen) |
| [**AppleALC**](https://github.com/acidanthera/AppleALC) |
| [**VirtualSMC**](https://github.com/acidanthera/VirtualSMC) |
| [**VoodooI2C**](https://github.com/VoodooI2C/VoodooI2C) |
| [**VoodooPS2**](https://github.com/acidanthera/VoodooPS2) |
| [**VoodooSMBus**](https://github.com/VoodooSMBus/VoodooSMBus) |
| [**VoodooRMI**](https://github.com/VoodooSMBus/VoodooRMI) |
| [**IntelBluetoothFirmware**](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) |
| [**AirportItlwm**](https://github.com/OpenIntelWireless/itlwm) |
| [**RealtekRTL8111**](https://github.com/Mieze/RTL8111_driver_for_OS_X) |
| [**VoodooInput**](https://github.com/acidanthera/VoodooInput) |
| [**RealtekCardReader**](https://github.com/0xFireWolf/RealtekCardReader) |
| [**ECEnabler**](https://github.com/1Revenger1/ECEnabler) |
| [**BrightnessKeys**](https://github.com/acidanthera/BrightnessKeys) |
| [**WhateverGreen**](https://github.com/acidanthera/WhateverGreen) |



### 🧰 实用工具 | Utilities
以下工具在配置和排错过程中不可或缺：
| 工具 |
| :--- | 
| [**ProperTree**](https://github.com/corpnewt/ProperTree) |
| [**OpenCore Configurator (OCC)**](https://mackie100projects.altervista.org/opencore-configurator/) | 
| [**Hackintool**](https://github.com/headkaze/Hackintool) |
| [**OCAT**](https://github.com/ic005k/OCAuxiliaryTools) |
| [**SSDTTime**](https://github.com/corpnewt/SSDTTime) |
| [**ssdtPRGen**](https://github.com/Piker-Alpha/ssdtPRGen.sh) |

### 📚 学习指南 | Guides & Resources
我们的配置深受以下卓越指南和社区资源的影响：
- **[Dortania‘s OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)** - OpenCore 安装指南。

*（如果您认为有项目被遗漏或链接有误，请通过邮件联系我们进行更新。）*


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
