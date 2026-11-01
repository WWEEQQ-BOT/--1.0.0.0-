# 贪吃蛇

基于 TypeScript、Vite、HTML Canvas 和 Electron 的贪吃蛇游戏。

## 开发

需要安装 Node.js 18 或更高版本。

```bash
npm install
npm run dev
```

按方向键或 WASD 移动，空格键或 Escape 暂停/继续。移动设备可以使用棋盘下方的方向按钮。

## 玩法

- **手动挑战**：用键盘或触屏控制绿色蛇。
- **AI 自动玩**：观察寻路 AI 自己寻找食物。
- **AI 人机对战**：绿色为玩家，蓝色为 AI；先撞到障碍的一方输。
- **难度**：轻松、标准、极速会调整游戏速度。
- **排行榜**：按玩法筛选，显示模式、难度、日期和对战 AI 得分；可确认后清空历史。成绩仅保存在本机。
- **音效**：点击右上角扬声器切换，偏好保存在浏览器中。

## 检查

```bash
npm test
npm run build
```

最高分、排行榜和音效偏好保存在浏览器的 localStorage 中。

## Windows 桌面版

需要 Windows 和 Node.js 18 或更高版本。首次打包前安装依赖：

```powershell
npm.cmd install
```

开发时运行 Electron 桌面窗口：

```powershell
npm.cmd run desktop:dev
```

同时生成 Windows 安装程序和免安装程序：

```powershell
npm.cmd run desktop:package
```

生成文件位于 `release` 目录：

- `贪吃蛇-1.0.0-x64-nsis.exe`：安装程序，可创建桌面和开始菜单快捷方式。
- `贪吃蛇-1.0.0-x64-portable.exe`：免安装便携版。

实际文件名会包含当前项目版本和构建架构。打包需要联网下载 Electron 运行时及打包依赖。
