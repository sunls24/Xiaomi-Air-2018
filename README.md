# 小米笔记本 Air 13.3 2018 款黑苹果 EFI 文件

[johnnync13](https://github.com/johnnync13/Xiaomi-Mi-Air) 的仓库已经非常完善了，但是目前对 macOS 11 以下的版本无法兼容，所以才有了此仓库。

- 在 johnnync13 的基础上精简和修改 SSDT 和 Kext 补丁
- 升级 OpenCore(0.7.6) 并修改了一些配置
- 升级所有 Kext 到最新版本

## 支持的版本
*在 release 界面下载对应版本， 唯一的区别是 `AirportItlwm.kext` 不同*
- [macOS 10.14 Mojave](https://github.com/sunls24/Xiaomi-Air-2018/releases?q=mojave&expanded=true)
- [macOS 10.15 Catalina](https://github.com/sunls24/Xiaomi-Air-2018/releases?q=catalina&expanded=true)
- [macOS 11.6 BigSur](https://github.com/sunls24/Xiaomi-Air-2018/releases?q=bigsur&expanded=true)
- [macOS 12.4 Monterey](https://github.com/sunls24/Xiaomi-Air-2018/releases?q=monterey&expanded=true) Opencore v2.8.1

## 工作
- WIFI
- 蓝牙
- USB
- 相机
- 触摸板
- 集成显卡
- 睡眠/唤醒
- 快捷按键（声音/亮度调节）
- 声卡（需使用 [johnnync13 Audio](https://github.com/johnnync13/Xiaomi-Mi-Air/tree/master/Audio) 仓库的 `ALCPlugFix` 脚本修复耳机声音问题）
- 原生电源管理（需解锁 CFG 锁，详情查看 [johnnync13 BIOS](https://github.com/johnnync13/Xiaomi-Mi-Air/tree/master/BIOS) 仓库中的说明）
- ...

## 不工作
- 独立显卡不可用
- 指纹解锁不可用

## 其他
- 开启 HIDPI：[https://github.com/xzhih/one-key-hidpi](https://github.com/xzhih/one-key-hidpi)，**可能需要先关闭 SIP**，如果无法开启，可尝试 [johnnync13 Display](https://github.com/johnnync13/Xiaomi-Mi-Air/tree/master/Display) 中的脚本
- 生成 CPUFriend 数据：[https://github.com/stevezhengshiqi/one-key-cpufriend](https://github.com/stevezhengshiqi/one-key-cpufriend) **建议安装完成后重新生成数据并替换原来的 Kext**
- 欠压设置参考 [johnnync13](https://github.com/johnnync13/Xiaomi-Mi-Air/tree/master/BIOS/VoltageShift) 仓库中的 `VoltageShift` 相关用法
- **生成序列号信息 (必须)**：使用 [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)，详细使用方法请参考[这里](https://dortania.github.io/OpenCore-Install-Guide/AMD/fx.html#platforminfo)
