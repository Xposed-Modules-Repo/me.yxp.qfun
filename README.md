<div align="center">
    <h1> QFun </h1>

![Downloads](https://img.shields.io/github/downloads/Xposed-Modules-Repo/me.yxp.qfun/total)
![GitHub Stars](https://img.shields.io/github/stars/oneQAQone/QFun?style=social)
[![Telegram Group](https://img.shields.io/badge/Telegram-Join_Group-2CA5E0?logo=telegram)](https://t.me/QFunChatGroup)
[![Telegram](https://img.shields.io/static/v1?label=Telegram&message=Channel&color=0088cc)](https://t.me/QFunChannel)
[![QQ Group](https://img.shields.io/badge/QQGroup-1067198087-12B7F5?style=style=for-the-badge&logo=tencentqq&logoColor=white)](https://qm.qq.com/cgi-bin/qm/qr?k=xLBeceHozik0J5LEpU3pEKH7fLWLqGCG&jump_from=webapi&authKey=3hAlEoISLQecIsNodlHwrmGkz6NupG1KNZ7mOy5E0d/Q8imzXMapXsNSVspPhku0)
</div>

# 简介
一个QQ/TIM功能性Xposed模块，设置及主页加号可见模块入口，不同帐号功能数据不互通

# 功能列表

### 模块功能
仅列举部分代表性功能，更多实用功能请在模块内探索：
- [x] 群打卡
- [x] 防撤回 (带提示)
- [x] 自动续火
- [x] 消息复读 (+1)
- [x] 闪照破解
- [x] 屏蔽艾特全体
- [x] 简洁群管菜单
- [x] 一键点赞
- [x] 上传 APK 重命名
- [x] 去除回复自动艾特
- [x] 平板模式
- [x] 显示精确消息时间
- [x] 自定义骰子/猜拳
- [x] 移除表情回应
- [x] 解除风险网页拦截

> 💡 如有其他功能需求欢迎提交反馈，具备可行性的功能将被加入开发计划。

### 脚本扩展与编写
模块内置基于 **BeanShell** 的脚本引擎，支持使用 **Java 语法** 编写脚本以动态扩展功能，可自行编写或从在线脚本库下载。

# 适配与运行环境

### Android 系统
*   **最低版本**: Android 8.0 (API Level 26)
*   **推荐版本**: Android 11.0+ (以获得最佳的 UI 适配体验)
*   **架构支持**: `arm64-v8a` (主流), `armeabi-v7a`。**暂不支持 x86 环境**（部分模拟器无法使用）。

### 宿主应用
| 应用 | 推荐版本 | 备注 |
| :--- | :--- | :--- |
| **QQ** | `v9.1.25` 及以上 | 其他基于 NT 架构的版本兼容性需自行测试 |
| **TIM** | `v4.0.95` 及以上 | 针对旧版架构做了部分兼容 |
> ⚠️ 新增功能主要基于最新版 QQ 开发，旧版本可能存在兼容性问题。

### 框架支持

| 环境类型 | 推荐方案 | 说明 |
| :--- | :--- | :--- |
| **✅ Root 环境** | **LSPosed (Zygisk/Riru)** | **强烈推荐**。支持 Scope 作用域模式，性能损耗最小，Hook 稳定性最高。 |
| **🛡️ 免 Root 环境** | **LSPatch 及主流免 Root 框架** | **推荐**。通过修补 APK 的方式集成 Xposed 环境，适合无法解锁 Bootloader 的设备。 |
| **⚡ Zygisk 模式** | **Zygisk** | **推荐**。无需依赖 LSPosed，通过 Zygisk 直接加载模块。⚠️ **不能与其他注入同一宿主的 LSPosed 模块同时使用**，否则可能发生 Hook 冲突、功能异常或闪退。 |
| *其他环境* | *EdXposed / 太极 / VMOS* | *理论支持*，但属于旧一代技术或容器环境，可能存在兼容性问题，未做全面测试。 |

# 反馈与日志

为了高效定位问题，反馈时**请务必注明**以下信息：
1.  **宿主版本**
2.  **模块版本**
3.  **运行框架及版本**

> **💡 提示**：`Android/data/[宿主包名]/QFun/global/log/` 目录下的 **environment_info.txt** 已自动记录了完整的运行环境信息，建议在反馈时一同提交。
> 您也可以直接打包并反馈 **LSPosed 框架日志**（建议开启详细日志）。

### 1. 常规错误
> 指功能异常、脚本报错等未导致应用闪退的情况。
*   **文件**: `error_log.txt`
*   **位置**: `Android/data/[宿主包名]/QFun/[当前QQ号]/log/`

### 2. 应用崩溃
> 指应用直接停止运行、闪退的情况。
*   **文件**: `crash_[时间戳].zip`
*   **位置**: `Android/data/[宿主包名]/QFun/[当前QQ号]/crash/`
    *   *(注：若未登录即闪退，请检查 `.../QFun/global/crash/` 目录)*
*   **提示**: 闪退弹窗中**点击路径文字**即可直接复制完整路径。

### ⚠️ 关于路径
请在设备的**内部存储**（若是应用分身/多开，则在对应的**分身存储**）中查找上述路径。

<div align="center">

*Made with ❤️ by [oneQAQone](https://github.com/oneQAQone)*

</div>
