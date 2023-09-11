# v2raya-flatpak

v2rayA flatpak 格式安装包(非官方)，可下载到 SteamDeck 安装使用。

# 在 SteamDeck 上的使用方法
**所有操作均需要切换到桌面模式**

## 确保你知道自己的密码
如果你没设置过自己的密码，打开终端执行 `passwd` 设置密码。

## 安装
```shell
# 添加仓库
flatpak remote-add --if-not-exists v2raya-flatpak https://glaumar.github.io/v2raya-flatpak/index.flatpakrepo

# 安装
flatpak install -y io.github.glaumar.v2raya_flatpak
```

## 手动启动
SteamDeck 每次开机后切换到桌面模式，点击应用图标启动（需要输入密码）。程序会在后台运行，启动完成或多次启动，会自动打开浏览器并访问 [localhost:2017](http://localhost:2017)。

## 设置/移除开机自启
在启动器里，右键点击应用图标，选择 Create/Remove v2raya-flatpak Service（需要输入密码）

![](./screenshots/screenshot1.png)

**注意：如果你设置了开机自启，在卸载 v2raya-flatpak 前最好执行一次移除操作**

# 为什么不上传到 Flathub ？

1. 非v2rayA官方项目，不保证持续更新；
2. flatpak 设计上不适合打包系统后台服务，打包成 flatpak 格式只是为了方便 SteamDeck 使用。

---
![](https://badges.pufler.dev/visits/glaumar/v2raya-flatpak)
