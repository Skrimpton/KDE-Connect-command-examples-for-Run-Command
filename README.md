> It's yet another list of KDE Connect command examples for "Run Command" 🙃

# `qdbus` commands
### Find <ins>*your*</ins> qdbus command
> if you want to replace `"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})"`, skipping the subshell
```
command -v qdbus qdbus{5,6} qdbus-qt{5,6}
```

## Volume (PC / System)

#### Volume - Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Up
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Mute
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "mute"
```

## Media 

#### Media - Seek Forward
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekforwardmedia
```
#### Media - Seek Forward (long)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekforwardmedialong
```
#### Media - Seek Backward
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekbackwardmedia
```
#### Media - Seek Backward (long)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut seekbackwardmedialong
```
#### Media - Play/Pause
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playpausemedia
```
#### Media - Next
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut nextmedia
```
#### Media - Previous
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut previousmedia
```
#### Media - Play
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playmedia
```
#### Media - Pause
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut pausemedia
```
#### Media - Stop
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut stopmedia
```
#### Media - Volume Up
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumeup
```
#### Media - Volume Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumedown
```


# Power management (Powerdevil) [`qdbus`]
## Screen

#### Decrease Screen Brightness
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Decrease Screen Brightness"
```
#### Decrease Screen Brightness (small)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Decrease Screen Brightness Small"
```
#### Increase Screen Brightness
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Increase Screen Brightness"
```
#### Increase Screen Brightness (small)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Increase Screen Brightness Small"
```
#### Turn Off Screen
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Turn Off Screen"
```


## Computer
PowerOff / PowerDown
- (Activates "When power button is pressed"-action): [Powerdevil docs](https://docs.kde.org/stable_kf6/en/powerdevil/kcontrol/powerdevil/index.html)
- Krunner/Kicker (start menu) -> Search: `Power Management`
- Krunner/Kicker (start menu) -> Search: `Shortcuts` -> Click `[System Settings] Shortcuts [Configure Keyboard Shortcuts]` -> [(Middle) Sidebar, under `System Services`]: `Power Management`
- [PowerOff / PowerDown explained: bug.kde.org](https://bugs.kde.org/show_bug.cgi?id=425915#c4)

#### Power Off 
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "PowerOff"
```
#### Power Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "PowerDown"
```
#### Hibernate
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Hibernate"
```
#### Sleep
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Sleep"
```
#### Power Profile
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "powerProfile"
```

## Keyboard

#### Increase Keyboard Brightness
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Increase Keyboard Brightness"
```
#### Decrease Keyboard Brightness
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Decrease Keyboard Brightness"
```
#### Toggle Keyboard Backlight
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/org_kde_powerdevil org.kde.kglobalaccel.Component.invokeShortcut "Toggle Keyboard Backlight"
```


# Other commands

## Screenshot to device / phone
Inspired by and building on: [Useful_commands#Screen_capture: kde userbase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands#Screen_capture)
> Can take little while (~5-20 seconds) after screenshot is taken by `spectacle`, before it's received on the phone

Dependencies:
- `spectacle`
- `kdeconnect-cli`
- `grep`
- `head`


### Auto-select top ID from active list and validate ID is active before sending
#### Screenshot - Fullscreen
```
kid="$(kdeconnect-cli -a --id-only | head -n 1)";  kdeconnect-cli --list-available --id-only | grep -x "${kid}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "$kid" --share "${file}" )
```
#### Screenshot - Active Window
```
kid="$(kdeconnect-cli -a --id-only | head -n 1)";  kdeconnect-cli --list-available --id-only | grep -x "${kid}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "$kid" --share "${file}" )
```

### Specify <ins>name</ins> and validate <ins>name</ins> is active before sending
#### Screenshot - Fullscreen
```
name="MY_DEVICE"; kdeconnect-cli --list-available --name-only | grep -x "${name}" &>/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -n "$name" --share "${file}" )
```
#### Screenshot - Active Window
```
name="MY_DEVICE"; kdeconnect-cli --list-available --name-only | grep -x "${name}" &>/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -n "${name}" --share "${file}" )
```


### Specify <ins>ID</ins> and validate <ins>ID</ins> is active before sending
#### Screenshot - Fullscreen
```
kid="MY_DEVICE"; kdeconnect-cli --list-available --id-only | grep -x "${kid}" &>/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "${kid}" --share "${file}" )
```
#### Screenshot - Active Window
```
kid="MY_DEVICE"; kdeconnect-cli --list-available --id-only | grep -x "${kid}" &>/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "${kid}" --share "${file}" )
```


## Sources
1. [userbase.kde.org - KDE UserBase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands)
1. [Guilherme (GuinuxBR)](https://github.com/guinuxbr/KDEConnect-commands/blob/main/commands.md)
