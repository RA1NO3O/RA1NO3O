## For macOS users:
### Install iOS apps/games which is not available for macOS(Apple Silicon only)
* Get and Install [PlayCover](https://playcover.io)
* Visit https://decrypt.day
### Enviornments:
```shell
### 移除app限制
removeAppLimit() {
  sudo xattr -r -d com.apple.quarantine $1
}

### 清除macOS DNS缓存
clearDNSCache() {
  sudo dscacheutil -flushcache
  sudo killall -HUP mDNSResponder
}

### 重设Dock栏大小
resetDockSize() {
  defaults delete com.apple.dock tilesize
  defaults delete com.apple.dock largesize
  killall Dock
}

### 重建启动台图标
resetLaunchPad () {
  defaults write com.apple.dock ResetLaunchPad -bool true
  killall Dock
}

### 打开macOS桌面壁纸文件夹
openDesktopWallpaper() {
  open "/System/Library/Desktop Pictures"
}

### 隐藏文件夹
hideFolder () {
  chflags hidden $1
}
q
### 取消隐藏文件夹
cancelHideFolder () {
  chflags nohidden $1
}

### 显示MetalHUD
showMetalHUD () {
  /bin/launchctl setenv MTL_HUD_ENABLED 1
}

### 隐藏MetalHUD
hideMetalHUD () {
  /bin/launchctl setenv MTL_HUD_ENABLED 0
}
```
----------------------------------------------------------------------------------------------
## For Windows users:
### Take common commands
* Set [Useful-Batch](https://github.com/RA1NO3O/Useful-Batch)
----------------------------------------------------------------------------------------------
## DDNS Updater for Google Domains
* https://github.com/RA1NO3O/gddns_updater_cli
