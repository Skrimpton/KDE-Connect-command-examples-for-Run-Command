# KDE-Connect-command-examples-for-Run-Command
> It's KDE Connect command examples for "Run Command" 🙃

## Find your qdbus version
```
command -v qdbus qdbus{5,6} qdbus-qt{5,6}
```

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

## Powerdevil (Power management) : Screen

#### Decrease Screen Brightness
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Decrease Screen Brightness"
```
#### Decrease Screen Brightness (small)
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Decrease Screen Brightness Small"
```
#### Increase Screen Brightness
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Increase Screen Brightness"
```
#### Increase Screen Brightness (small)
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Increase Screen Brightness Small"
```

## Powerdevil (Power management) : PowerOff / PowerDown

- (Activates "When power button is pressed"-action): [Powerdevil docs](https://docs.kde.org/stable_kf6/en/powerdevil/kcontrol/powerdevil/index.html)
- Krunner/Kicker (start menu) -> Search: "Power Management"
- ["PowerOff"/"PowerDown" explained: bug.kde.org](https://bugs.kde.org/show_bug.cgi?id=425915#c4)

#### Power Off 
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "PowerOff"
```
#### Power Down
```
qdbus6 org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "PowerDown"
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


## Sources
1. [userbase.kde.org - KDE UserBase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands)
1. [Guilherme (GuinuxBR)](https://github.com/guinuxbr/KDEConnect-commands/blob/main/commands.md)
