# KDE-Connect-command-examples-for-Run-Command

- It's KDE Connect command examples for "Run Command"

- You can replace `"$(command -v qdbus qdbus5 qdbus6 | head -n1)"` with the qdbus command on your system, this is just the most generalized

## Sources
1. [userbase.kde.org - KDE UserBase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands)


## Volume (PC / System)
#### Volume - Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Up
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Mute
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.kglobalaccel /component/kmix invokeShortcut "mute"
```

## Media
#### Media - Seek Forward
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekforwardmedia
```
#### Media - Seek Forward (long)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekforwardmedialong
```
#### Media - Seek Backward
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekbackwardmedia
```
#### Media - Seek Backward (long)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekbackwardmedialong
```
#### Media - Play/Pause
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6} | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playpausemedia
```

#### Media - Next
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut nextmedia
```

#### Media - Previous
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut previousmedia
```

#### Media - Play
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playmedia
```

#### Media - Pause
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut pausemedia
```

#### Media - Stop
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut stopmedia
```

#### Media - Volume Up
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumeup
```

#### Media - Volume Down
```
"$(command -v qdbus qdbus5 qdbus6 | head -n1)" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumedown
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
