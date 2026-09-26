# 桌面鱼缸

一个会回应你的 macOS 动态鱼缸。鱼群会避让光标、争抢食物；水草、海葵和悬浮颗粒随水流缓慢摆动。默认场景是珊瑚海，也可从菜单栏切换到水草溪流。

场景使用 Three.js 与 WebGL2 实时渲染，所有资源均随应用打包。安装完成后无需账号或网络连接。

## 立即预览

需要 Node.js 20 或更高版本：

```sh
npm start
```

然后打开终端显示的本地地址。浏览器内可点击水面投喂；移动鼠标可与鱼群互动。快捷键：

- `Space`：暂停或继续
- `F`：进入或退出全屏
- `H`：隐藏或显示控制栏

画质提供节能（20 fps）、均衡（30 fps）和精细（60 fps）三档。

## 安装为 macOS 动态壁纸

要求 macOS 13 或更高版本，以及 Xcode Command Line Tools：

```sh
xcode-select --install
sh wallpaper/install.sh
```

安装脚本会编译并安装 `~/Applications/Desktop Aquarium.app`，随后添加登录启动项。首次显示通常需要约 20 秒。

菜单栏中的鱼形图标可用于：

- 在“珊瑚海”和“水草溪流”之间切换
- 向每块显示器上的鱼缸投喂
- 暂停或继续动画
- 退出应用

动态壁纸位于桌面图标下方，不拦截点击或拖拽。应用支持多显示器，并会在桌面几乎完全被窗口遮挡、屏幕锁定、进入睡眠或开启低电量模式时停止渲染。

卸载：

```sh
sh wallpaper/uninstall.sh
```

## 隐私

应用只读取全局光标位置以驱动鱼群互动，并读取窗口的位置与尺寸以估算桌面可见面积。它不会读取窗口内容、记录光标轨迹或发送分析数据，也不申请辅助功能、输入监控或录屏权限。

## 开源来源与许可证

本项目基于 Chase Lean 的 [Desktop Habitats](https://github.com/chaseleantj/desktop-habitats) 改编，沿用了其 macOS 壁纸宿主、生态模拟与程序化场景实现，并重新设置了产品名称、默认体验和中文界面。

项目代码遵循 [MIT License](LICENSE)。Three.js 的许可证见 [vendor/THREE-LICENSE.txt](vendor/THREE-LICENSE.txt)。岩石、木材与沙地纹理来自 Poly Haven，采用 CC0 许可；珊瑚场景的岩体、纹理与生物模型由仓库内工具程序化生成。
