# Popsicle_Kernel: Xiaomi 17 (Popsicle) 自动构建项目 🚀

![Kernel Build Status](https://img.shields.io/github/actions/workflow/status/wjx-wp/Popsicle_Kernel/build.yml?branch=popsicle-w-oss&label=Build%20Status&style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Qualcomm%20SM8850-orange?style=for-the-badge)
![Android Version](https://img.shields.io/badge/Android-W%20(16)-green?style=for-the-badge)

本项目致力于通过 GitHub Actions 实现小米 17 Pro Max (代号: **Popsicle**) 内核的自动化云编译，并深度集成下一代 Root 方案 **SukiSU** 与 **SUSFS**。

---

## 🌟 项目特性

* **设备型号**: 小米 17 Pro Max (代号: popsicle / canoe 平台)
* **内核版本**: 基于 Google GKI 6.12 架构 (Android 16 / W)
* **集成组件**:
    * **SukiSU**: 性能极佳、隐蔽性更强的 Root 框架。
    * **SUSFS**: 强大的内核级文件隐藏支持，轻松通过各项安全检测。
* **构建系统**: 采用高通/小米最新的 **Kleaf (Bazel)** 模块化构建。

---

## 🛠️ 如何使用 (对于用户)

你可以直接 Fork 本仓库，利用 GitHub Actions进行编译。

1.  **Fork** 本仓库到你的账号下。
2.  进入你仓库顶部的 **Actions** 选项卡。
3.  在左侧选择 `Build Popsicle Kernel with SukiSU + SUSFS`。
4.  点击右侧的 **Run workflow**。
5.  等待约 1 小时，编译完成后在 `Artifacts` 处下载产生的 `.zip` 刷机包。

---

## 🚧 目前进展 (Current Progress)

* [x] **基础设施**: 成功搭建 GitHub Actions 云端 Kleaf 构建环境。
* [x] **拓扑解析**: 破解小米 17 多仓库 (Multi-repo) 依赖结构。
* [x] **组件集成**: 成功将 SukiSU 补丁注入 GKI 核心。
* [ ] **正在攻克**: 修复 Bazel 编译过程中的模块加载路径冲突 (`.bzl` 文件缺失问题)。
* [ ] **待完成**: 首次成功产出可引导的 `Image`。

---

## 🤝 欢迎贡献 (Contributing)

由于小米 17系列 采用了全新的模块化内核设计，个人维护压力较大，非常欢迎大佬提交 **Pull Request**！

**我们需要帮助的方向：**
1.  **子模块同步**: 优化 `Xiaomi_Kernel_OpenSource` 及其碎片化驱动仓库的同步脚本。
2.  **编译调优**: 解决 Bazel 在云端环境下的 OOM 或资源限制问题。
3.  **机型适配**: 欢迎添加更多基于 `canoe` 平台的机型配置文件。

---

## ⚠️ 免责声明

* 本内核仅供学习交流使用，由于解开 Bootloader 或刷入第三方内核导致的保修失效、硬件损坏或数据丢失，本项目概不负责。
* 请务必提前做好数据备份。

---

## 💖 鸣谢

* [MiCode/Xiaomi_Kernel_OpenSource](https://github.com/MiCode/Xiaomi_Kernel_OpenSource)
* [SukiSU-Ultra Project](https://github.com/SukiSU-Ultra)
* [GKI (Google Kernel Infrastructure)](https://source.android.com/devices/architecture/kernel/generic-kernel-image)
* [sid7711/susfs4ksu (GitLab)](https://gitlab.com/sid7711/susfs4ksu)
