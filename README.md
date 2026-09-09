# 雨课堂自动播放助手

[![Version](https://img.shields.io/badge/version-3.1.0-blue.svg)](https://github.com/Breeze1733/yuketang-auto-player)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Tampermonkey%20%7C%20Violentmonkey%20%7C%20ScriptCat-orange.svg)](https://www.tampermonkey.net/)
[![Target](https://img.shields.io/badge/target-yuketang.cn-informational.svg)](https://www.yuketang.cn/)

专为**雨课堂（yuketang.cn / gdufemooc.cn）**打造的全版本视频与课件自动播放辅助工具。

本脚本专注于**课程视频与课件的自动播放**，支持倍速调节、自动下一集、后台防暂停等实用特性。遇到作业、测验与考试等答题节点时均会自动跳过，仅支持音视频与课件的自动播放。

**如果您觉得本项目有用，请给这个项目一个 Star ⭐**

---

## 🚀 面向用户：一键安装

无需配置任何复杂的开发环境，只要浏览器已安装油猴扩展，点击下方按钮即可一键安装：

[![一键安装 - GitHub 官方源](https://img.shields.io/badge/一键安装-GitHub%20官方源-00485B?style=for-the-badge&logo=tampermonkey&logoColor=white)](https://raw.githubusercontent.com/Breeze1733/yuketang-auto-player/main/yuketang.user.js)

[![国内镜像 - 一键安装](https://img.shields.io/badge/国内镜像-一键安装%20(推荐国内网络)-FF5627?style=for-the-badge&logo=jsdelivr&logoColor=white)](https://cdn.jsdelivr.net/gh/Breeze1733/yuketang-auto-player@main/yuketang.user.js)

> 💡 **提示**：若点击 GitHub 官方源无法加载或速度较慢，推荐点击 **【国内镜像一键安装】**（由 jsDelivr CDN 加速提供）。

### 前置准备

若你的浏览器尚未安装脚本管理器，推荐先安装以下任一扩展（已安装请忽略）：
* [Tampermonkey（篡改猴 - Chrome 商店）](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
* [Tampermonkey（Edge 扩展中心）](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd)
* 或 [Violentmonkey（暴力猴）](https://violentmonkey.github.io/) / [ScriptCat（脚本猫）](https://docs.scriptcat.org/)

安装好扩展后，点击上方 **【一键安装】** 链接，在弹出的窗口中点击 **“安装”** 或 **“更新”** 即可。

---

## 🎬 功能定位与特性

### 1. 专注于视频与课件播放
* **仅支持音视频与课件**：脚本定位明确，专注处理音视频播放与课件浏览，轻量且稳定；
* **自动跳过作业与测验**：执行过程中检测到作业、测验、考试等答题节点时，均会**自动跳过**并直接推进至下一节视频；
* **极简轻量**：无需加载多余外部第三方依赖，脚本秒开加载，占用极低。

### 2. 雨课堂全版本自适应
* **v2 经典版**：支持 `/v2/web/studentLog/*` 等列表界面与视频学习；
* **pro / lms 专业版**：支持 `/pro/lms/*` 平台视频自动连播与下一节推进；
* **ai-workspace 新版学习空间**：支持 `/ai-workspace/lms-graph/*` 知识图谱界面的音视频自动流转与课件播放；
* **定制版支持**：兼容广东金融学院定制版雨课堂（`*.gdufemooc.cn`）等相同架构的雨课堂子站。

### 3. 播放器增强与后台挂机
* **自定义倍速调节**：默认 2.0x 倍速播放，支持通过内置面板随时切换 1.0x / 1.25x / 1.5x / 2.0x；
* **自动静音与防暂停**：接管播放器静音，定时监听防异常暂停并自动恢复播放；
* **PPT 课件自动翻页**：自动计算课件停留时间并按设定的间隔逐页浏览，播放完毕自动返回；
* **后台防切屏与弹窗自动关闭**：规避失焦与切屏暂停检测，自动处理“好好学习/继续观看”等防挂机弹窗。

---

## 📖 使用方法

1. 登录雨课堂网页端（或对应学校定制雨课堂站点），进入具体课程的学习内容页面；
2. 页面左上方会自动加载控制面板（支持鼠标拖动标题栏移动位置，或点击右上角 `_` 最小化为小球浮窗）；
3. **播放设置**：如需修改倍速或课件翻页时长，点击面板底部的 **【播放设置】** 进行调整并保存；
4. **开始刷课**：点击面板底部的 **【开始刷课】** 按钮，脚本将自动接管播放、显示实时进度并自动跳转下一集；
5. **停止播放**：如需中途暂停，点击 **【停止刷课】** 即可刷新恢复正常状态。

---

## 免责声明

用户脚本（Userscript）是一种程序，通常用 JavaScript 编写，可用于修改网页代码以增强用户的浏览体验。具体用途有添加网页的快捷按钮，控制视频播放速度以及为网站添加其他功能。 在 Firefox 浏览器等桌面浏览器上，Userscript 是通过浏览器扩充功能中的脚本管理器（例如 Greasemonkey ）启用的。

此项目作为开源的用户脚本，遵循用户脚本的编写规范，并且使用纯粹的 javascript 执行代码，不对页面进行任何源码的修改，不附加任何等非法入侵计算机系统的功能，不对客户端计算机进行任何破坏越权控制等行为。

该项目作为开源用户脚本，供各大用户学习、交流、参考、使用，项目所有功能均为开源免费，如果存在收费功能则为其他项目，对于所造成的任何费用损失不负任何责任。

使用本项目即代表用户对此项目的源码和功能有一定的了解，对于所造成的一切后果均由用户自己承担。

---

## 📄 许可协议

本项目基于 [MIT License](LICENSE) 开源。
