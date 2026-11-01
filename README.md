# KDE-Connect-command-examples-for-Run-Command

- It's KDE Connect command examples for "Run Command"

- You can replace `qdbus6` with your own: `command -v qdbus qdbus{5,6} qdbus-qt{5,6}`


## Sources
1. [userbase.kde.org - KDE UserBase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands)
1. [Guilherme (GuinuxBR)](https://github.com/guinuxbr/KDEConnect-commands/blob/main/commands.md)

## Volume (PC / System)

#### Volume - Down
```
qdbus6 org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Up
```
qdbus6 org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Mute
```
qdbus6 org.kde.kglobalaccel /component/kmix invokeShortcut "mute"
```

## Media

#### Media - Seek Forward
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekforwardmedia
```
#### Media - Seek Forward (long)
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekforwardmedialong
```
#### Media - Seek Backward
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekbackwardmedia
```
#### Media - Seek Backward (long)
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekbackwardmedialong
```
#### Media - Play/Pause
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playpausemedia
```
#### Media - Next
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut nextmedia
```
#### Media - Previous
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut previousmedia
```
#### Media - Play
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playmedia
```
#### Media - Pause
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut pausemedia
```
#### Media - Stop
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut stopmedia
```
#### Media - Volume Up
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumeup
```
#### Media - Volume Down
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumedown
```

## Powerdevil (Power management)

#### Decrease Screen Brightness (small)
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Decrease Screen Brightness Small"
```
#### Increase Screen Brightness (small)
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Increase Screen Brightness Small"
```


## Screenshot to phone (Auto-selects top id from active list)
##### Dependencies:
- `spectacle`
- `kdeconnect-cli`
- `head`
#### Screenshot - Fullscreen
```
kid="$(kdeconnect-cli -a --id-only | head -n 1)"; [ -n ${kid} ] && file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "$kid" --share "${file}"
```
#### Screenshot - Active Window
```
kid="$(kdeconnect-cli -a --id-only | head -n 1)"; [ -n ${kid} ] && file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "$kid" --share "${file}"
```
