# :bird: pterodactyl-installer

![Test Panel](https://github.com/pterodactyl-installer/pterodactyl-installer/actions/workflows/panel.yml/badge.svg)
![Test Wings](https://github.com/pterodactyl-installer/pterodactyl-installer/actions/workflows/wings.yml/badge.svg)
![Shellcheck](https://github.com/pterodactyl-installer/pterodactyl-installer/actions/workflows/shellcheck.yml/badge.svg)
[![License: GPL v3](https://img.shields.io/github/license/pterodactyl-installer/pterodactyl-installer)](LICENSE)
[![Discord](https://img.shields.io/discord/682342331206074373?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://pterodactyl-installer.se/discord)
[![made-with-bash](https://img.shields.io/badge/-Made%20with%20Bash-1f425f.svg?logo=image%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyZpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw%2FeHBhY2tldCBiZWdpbj0i77u%2FIiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8%2BIDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNi1jMTExIDc5LjE1ODMyNSwgMjAxNS8wOS8xMC0wMToxMDoyMCAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIDIwMTUgKFdpbmRvd3MpIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOkE3MDg2QTAyQUZCMzExRTVBMkQxRDMzMkJDMUQ4RDk3IiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOkE3MDg2QTAzQUZCMzExRTVBMkQxRDMzMkJDMUQ4RDk3Ij4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6QTcwODZBMDBBRkIzMTFFNUEyRDFEMzMyQkMxRDhEOTciIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6QTcwODZBMDFBRkIzMTFFNUEyRDFEMzMyQkMxRDhEOTciLz4gPC9yZGY6RGVzY3JpcHRpb24%2BIDwvcmRmOlJERj4gPC94OnhtcG1ldGE%2BIDw%2FeHBhY2tldCBlbmQ9InIiPz6lm45hAAADkklEQVR42qyVa0yTVxzGn7d9Wy03MS2ii8s%2BeokYNQSVhCzOjXZOFNF4jx%2BMRmPUMEUEqVG36jo2thizLSQSMd4N8ZoQ8RKjJtooaCpK6ZoCtRXKpRempbTv5ey83bhkAUphz8fznvP8znn%2B%2F3NeEEJgNBoRRSmz0ub%2FfuxEacBg%2FDmYtiCjgo5NG2mBXq%2BH5I1ogMRk9Zbd%2BQU2e1ML6VPLOyf5tvBQ8yT1lG10imxsABm7SLs898GTpyYynEzP60hO3trHDKvMigUwdeaceacqzp7nOI4n0SSIIjl36ao4Z356OV07fSQAk6xJ3XGg%2BLCr1d1OYlVHp4eUHPnerU79ZA%2F1kuv1JQMAg%2BE4O2P23EumF3VkvHprsZKMzKwbRUXFEyTvSIEmTVbrysp%2BWr8wfQHGK6WChVa3bKUmdWou%2BjpArdGkzZ41c1zG%2Fu5uGH4swzd561F%2BuhIT4%2BLnSuPsv9%2BJKIpjNr9dXYOyk7%2FBZrcjIT4eCnoKgedJP4BEqhG77E3NKP31FO7cfQA5K0dSYuLgz2TwCWJSOBzG6crzKK%2BohNfni%2Bx6OMUMMNe%2Fgf7ocbw0v0acKg6J8Ql0q%2BT%2FAXR5PNi5dz9c71upuQqCKFAD%2BYhrZLEAmpodaHO3Qy6TI3NhBpbrshGtOWKOSMYwYGQM8nJzoFJNxP2HjyIQho4PewK6hBktoDcUwtIln4PjOWzflQ%2Be5yl0yCCYgYikTclGlxadio%2BBQCSiW1UXoVGrKYwH4RgMrjU1HAB4vR6LzWYfFUCKxfS8Ftk5qxHoCUQAUkRJaSEokkV6Y%2F%2BJUOC4hn6A39NVXVBYeNP8piH6HeA4fPbpdBQV5KOx0QaL1YppX3Jgk0TwH2Vg6S3u%2BdB91%2B%2FpuNYPYFl5uP5V7ZqvsrX7jxqMXR6ff3gCQSTzFI0a1TX3wIs8ul%2Bq4HuWAAiM39vhOuR1O1fQ2gT%2F26Z8Z5vrl2OHi9OXZn995nLV9aFfS6UC9JeJPfuK0NBohWpCHMSAAsFe74WWP%2BvT25wtP9Bpob6uGqqyDnOtaeumjRu%2ByFu36VntK%2FPA5umTJeUtPWZSU9BCgud661odVp3DZtkc7AnYR33RRC708PrVi1larW7XwZIjLnd7R6SgSqWSNjU1B3F72pz5TZbXmX5vV81Yb7Lg7XT%2FUXriu8XLVqw6c6XqWnBKiiYU%2BMt3wWF7u7i91XlSEITwSAZ%2FCzAAHsJVbwXYFFEAAAAASUVORK5CYII%3D)](https://www.gnu.org/software/bash/)

非正式的腳本，用於安裝 Pterodactyl Panel 與 Wings，適用於最新版本的 Pterodactyl！

想了解更多關於 [Pterodactyl](https://pterodactyl.io/) 的資訊請看在這裡。这个腳本並非由官方 Pterodactyl 項目關聯或認可。

## 特色

- 自動安裝 Pterodactyl Panel (dependencies, database, cronjob, nginx)。
- 自動安裝 Pterodactyl Wings (Docker, systemd)。
- Panel：（選擇性）Let's Encrypt 自動配置。
- Panel：（選擇性）firewall 自動配置。
- 支援 Panel 和 Wings 二者的刪除功能。

## 協助與支持

關於腳本本身的協助與支持，而非官方 Pterodactyl 項目，您可以加入 [Discord 聊天室](https://pterodactyl-installer.se/discord).

## 支援的安裝

panel 和 Wings 支援的安裝設定清單（此安裝腳本支援的安裝）。

### 支援的 panel 和 Wings 操作系統

| 操作系統          | 版本    | 是否支援            | PHP 版本    |
| ---------------- | ------- | ------------------ | ----------- |
| Ubuntu           | 14.04   | :red_circle:       |             |
|                  | 16.04   | :red_circle: \*    |             |
|                  | 18.04   | :red_circle: \*    | 8.1         |
|                  | 20.04   | :white_check_mark: | 8.1         |
|                  | 22.04   | :white_check_mark: | 8.1         |
|                  | 24.04   | :white_check_mark: | 8.1         |
| Debian           | 8       | :red_circle: \*    |             |
|                  | 9       | :red_circle: \*    |             |
|                  | 10      | :white_check_mark: | 8.1         |
|                  | 11      | :white_check_mark: | 8.1         |
|                  | 12      | :white_check_mark: | 8.1         |
| CentOS           | 6       | :red_circle:       |             |
|                  | 7       | :red_circle: \*    |             |
|                  | 8       | :red_circle: \*    |             |
| Rocky Linux      | 8       | :white_check_mark: | 8.1         |
|                  | 9       | :white_check_mark: | 8.1         |
| AlmaLinux        | 8       | :white_check_mark: | 8.1         |
|                  | 9       | :white_check_mark: | 8.1         |

_\* 表示此指令碼之前支援的操作系統與版本。_

## 使用安裝腳本

要使用安裝腳本，只需以 root 身分執行此命令。腳本會詢問您是想僅安裝面板、僅安裝 Wings 還是都安裝。

```bash
bash <(curl -s https://pterodactyl-installer.se)
```

_注意：在某些系統上，您需要在執行一行式命令前已經以 root 身分登入（即使命令前面有 sudo 也是不起作用的）。_

這是一個 [YouTube](https://www.youtube.com/watch?v=E8UJhyUFoHM) 影片，展示安裝過程。

## 防火牆設置

安裝腳本可以為您安裝和配置防火牆。腳本將詢問您是否要這樣做。強烈建議選擇自動防火牆設置。

## 開發與運營

### 在本地測試腳本

為了測試腳本，我們使用 [Vagrant](https://www.vagrantup.com)。用 Vagrant，你可以快速啟動並運行一個新鮮的機器來測試這腳本。

如果您想一次性在所有支援的安裝環境中測試腳本，只需執行如下命令。

```bash
vagrant up
```

如果您只想測試特定發行版，可以執行下列命令。

```bash
vagrant up <name>
```

將名稱替換為以下內容之一（支援的安裝）。

- `ubuntu_jammy`
- `ubuntu_focal`
- `debian_bullseye`
- `debian_buster`
- `debian_bookworm`
- `almalinux_8`
- `almalinux_9`
- `rockylinux_8`
- `rockylinux_9`

隨後，您可以使用 `vagrant ssh <機器名稱>` 來 SSH 進入機器。該專案目錄會被挂载在 `/vagrant`，這能讓您迅速在本地上修改腳本，然後通過分別執行 `/vagrant/installers/panel.sh` 和 `/vagrant/installers/wings.sh` 指令文檔来測試变更。

### 創建版本發行

在 `install.sh` 中，GitHub 來源和脚本版本變量每個版本都應該做出改變。首先，更新 `CHANGELOG.md` 文件，使版本發行的日期和版本標籤（Release Tag）都能顯示出來。對於變更記錄的項目本身不应该做任何更改。其次，更新 `install.sh` 中的 `GITHUB_SOURCE` 和 `SCRIPT_RELEASE` 變量。最後，您現在可以提交一個具有消息 `Release vX.Y.Z` 的提交。之後，創建 GitHub 上的版本發布。[this commit](https://github.com/pterodactyl-installer/pterodactyl-installer/commit/90aaae10785f1032fdf90b216a4a8d8ca64e6d44) 這個提交。

## 貢獻者 ✨

版权所有 © 2018 - 2024，Vilhelm Prytz，vilhelm@prytznet.se，以及所有貢獻者！

- Created by [Vilhelm Prytz](https://github.com/vilhelmprytz)
- Maintained by [Linux123123](https://github.com/Linux123123)

Thanks to the Discord moderators [sam1370](https://github.com/sam1370), [Linux123123](https://github.com/Linux123123) and [sinjs](https://github.com/sinjs) for helping on the Discord server!
contributors
