# Popsicle_Kernel: Xiaomi 17 (Popsicle) 自动构建项目 

![Kernel Build Status](https://img.shields.io/github/actions/workflow/status/wjx-wp/Popsicle_Kernel/build.yml?branch=popsicle-w-oss&label=Build%20Status&style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Qualcomm%20SM8850-orange?style=for-the-badge)
![Android Version](https://img.shields.io/badge/Android-W%20(16)-green?style=for-the-badge)

本项目致力于通过 GitHub Actions 实现小米 17 (代号: **Popsicle**) 内核的自动化云编译，并深度集成下一代 Root 方案 **SukiSU** 与 **SUSFS**。

---

##  项目特性

* **设备型号**: 小米 17 / 小米 17 Pro (代号: popsicle / canoe 平台)
* **内核版本**: 基于 Google GKI 6.12 架构 (Android 16 / W)
* **集成组件**:
    * **SukiSU**: 性能极佳、隐蔽性更强的 Root 框架。
    * **SUSFS**: 强大的内核级文件隐藏支持。
* **构建系统**: 采用高通/小米最新的 **Kleaf (Bazel)** 模块化构建。

---

##  目前进展 (Current Progress)

* [x] **基础设施**: 成功搭建 GitHub Actions 云端 Kleaf 构建环境。
* [x] **拓扑解析**: 破解小米 17 多仓库 (Multi-repo) 依赖结构。
* [x] **组件集成**: 成功将 SukiSU 补丁注入。
* [ ] **正在攻克**: 修复子模块缺失导致的 .bzl 加载失败问题（--recursive 同步中）。
* [ ] **待完成**: 首次成功产出可引导的 `Image`。

---

##  欢迎贡献 (Contributing)

小米 17 采用了复杂的模块化设计，欢迎社区大佬提交 **Pull Request** 协助优化构建脚本！

---

##  免责声明

* 本项目仅供学习交流，刷机有风险，操作需谨慎。
