# FirstPace

一个自己的AIGC小实验, 目标是一个Ubuntu/Windows/Android可用的时间任务管理应用.

## 目录结构

```
firstpace/          # 打包目录，包含应用安装结构
  DEBIAN/               # Debian 包控制文件
  usr/
    bin/firstpace   # 主执行脚本
    share/
      applications/     # 桌面文件
      icons/            # 应用图标
```

根目录还有一个 `build.sh` 用于生成 `.deb` 包。

## 依赖

- Python 3
- `python3-gi` 和 GTK+ 3（`gir1.2-gtk-3.0`）

## 开发与运行

1. 确保安装依赖：
   ```bash
   sudo apt install python3-gi gir1.2-gtk-3.0
   ```

2. 直接运行脚本（开发模式）：
   ```bash
   python3 firstpace/usr/bin/firstpace
   ```

3. 编译生成 Debian 包：
   ```bash
   ./build.sh
   ```
   生成的包在根目录下，如 `firstpace_1.0.0_all.deb`。

## 发布

使用 `dpkg -i` 安装生成的 `.deb` 包，或者将包上传到 APT 仓库。

## 未来展望
### 具体见 pull request #6
- 支持 Windows 和 Android 平台
- 增加更多功能，如日历/课表/日程等
- 可以导入学校课表吗...?!
- 优化用户界面和用户体验
- maybe一点点奖励机制 (point system, or 年月日的成就log)
- 心流辅助设计
- 免打扰模式

