> It's yet another list of KDE Connect command examples for "Run Command" 🙃
# Table of contents
| Title | payload action |
|---|---|
| [Find *your* qdbus command](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-your-qdbus-command) |
| [Sound (PC / System)](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#sound-pc--system-qdbus) | `qdbus` |
| [Media Controls](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#media-controls-qdbus) | `qdbus` |
| [Power management - Screen](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#power-management---screen) | `qdbus` |
| [Power management - Computer](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#power-management---computer) | `qdbus` |
| [Power management - Keyboard](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#power-management---keyboard-lights) | `qdbus` |
| [Find available devices using `kdeconnect-cli`](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-available-devices-using-kdeconnect-cli) |
| [Screenshot to device / phone](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#screenshot-to-device--phone) | `kdeconnect-cli --share`  |
| [Weather ping](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#weather-ping---specify-name-like-above) | `kdeconnect-cli --ping-msg` |

# `qdbus` commands
### Find <ins>*your*</ins> qdbus command
> if you want to replace `"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})"`, skipping the subshell
```
command -v qdbus qdbus{5,6} qdbus-qt{5,6}
```
<br>

# Sound (PC / System) [`qdbus`]

#### Volume - Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Down (small)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume_small"
```
#### Volume - Up
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_volume"
```
#### Volume - Up (Small)
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "increase_volume_small"
```
#### Volume - Mute
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "mute"
```
#### Microphone - Up
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "increase_microphone_volume"
```
#### Microphone - Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "decrease_microphone_volume"
```
#### Microphone - Mute
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "mic_mute"
```
#### Microphone - Push to Talk
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.kglobalaccel /component/kmix invokeShortcut "push_to_talk"
```
<br>

# Media Controls [`qdbus`]

#### Media - Play/Pause
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut playpausemedia
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
#### Media - Next
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut nextmedia
```
#### Media - Previous
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut previousmedia
```
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
#### Media - Volume Up
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumeup
```
#### Media - Volume Down
```
"$(command -v qdbus qdbus{5,6} qdbus-qt{5,6})" org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut mediavolumedown
```
<br>

# Power management (Powerdevil) [`qdbus`]

<br>

## Power management - Screen

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
<br>

## Power management - Computer
PowerOff / PowerDown
- (Activates "When power button is pressed"-action): [Powerdevil docs](https://docs.kde.org/stable_kf6/en/powerdevil/kcontrol/powerdevil/index.html)
> HOWTO: Find the system settings tab for Power Management
>  1. Open Krunner or Application Launcher/Dashboard/Menu (start menu)
>  2. Search and click:<br>`Power Management`<br>[Category: System Settings]
- [PowerOff / PowerDown explained: bugs.kde.org](https://bugs.kde.org/show_bug.cgi?id=425915#c4)

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
<br>

## Power management - Keyboard lights

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
<br>

# Other commands
#### Find available devices using `kdeconnect-cli`
```
kdeconnect-cli --list-available
```
<br>

## Screenshot to device / phone
<table>
  <head>Dependencies</head>
  <tr>
    <td><code>spectacle</code></td>
    <td><code>kdeconnect-cli</code></td>
    <td><code>grep</code></td>
    <td><code>head</code></td>
  </tr>
</table>

Inspired by and building on: [Useful_commands#Screen_capture: kde userbase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands#Screen_capture)
> Can take little while (~5-20 seconds) after screenshot is taken by `spectacle`, before it's received on the phone

### Auto-select top ID from active list and validate ID is active before sending
#### Screenshot - Fullscreen
```
kid="$(kdeconnect-cli -a --id-only | head -n 1)";  kdeconnect-cli --list-available --id-only | grep -x "${kid}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "$kid" --share "${file}" )
```
#### Screenshot - Active Window
```
kid="$(kdeconnect-cli -a --id-only | head -n 1)";  kdeconnect-cli --list-available --id-only | grep -x "${kid}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "$kid" --share "${file}" )
```

### [Specify](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-available-devices-using-kdeconnect-cli) *ID* and validate *ID* is active before sending
#### Screenshot - Fullscreen
```
kid="MY_DEVICE_ID"; kdeconnect-cli --list-available --id-only | grep -x "${kid}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "${kid}" --share "${file}" )
```
#### Screenshot - Active Window
```
kid="MY_DEVICE_ID"; kdeconnect-cli --list-available --id-only | grep -x "${kid}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -d "${kid}" --share "${file}" )
```

### [Specify](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-available-devices-using-kdeconnect-cli) *name*, and validate *name* is active before sending
#### Screenshot - Fullscreen
```
name="MY_DEVICE"; kdeconnect-cli --list-available --name-only | grep -x "${name}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -bo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -n "$name" --share "${file}" )
```
#### Screenshot - Active Window
```
name="MY_DEVICE"; kdeconnect-cli --list-available --name-only | grep -x "${name}" >/dev/null && ( file="/tmp/ScreenshotKDEConnect_$(date "+%Y%m%d_%H%M%S").png"; spectacle -abo "${file}" && while ! [ -f "${file}" ]; do sleep 0.3; done && kdeconnect-cli -n "${name}" --share "${file}" )
```
<br>

## Weather ping - ([Specify](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-available-devices-using-kdeconnect-cli) *name*, like above)
```
name="MY_DEVICE"; place=LONDON; underline="————"; lat="51.50853"; lon="-0.12574"; url="https://api.met.no/weatherapi/locationforecast/2.0/compact?lat=${lat}&lon=${lon}"; weather="$(curl -s "${url}" | jq -r '.properties.timeseries[0] | "Time: \(.time)\nTemp: \(.data.instant.details.air_temperature)°C\nWeather: \(.data.next_1_hours.summary.symbol_code)\nPrecipitation: \(.data.next_1_hours.details.precipitation_amount)mm"')"; kdeconnect-cli --list-available --name-only | grep -x "${name}" >/dev/null && ( kdeconnect-cli -n "${name}" --ping-msg "$(printf '%s\n%s\n%s' "${place}" "${underline}" "${weather}")" )
```

<table>
  <head>Dependencies</head>
  <tr>
    <td><code>curl</code></td>
    <td><code>jq</code></td>
    <td><code>kdeconnect-cli</code></td>
    <td><code>printf</code></td>
  </tr>
</table>

| Weather sources | Output example¹ | How to find `lat` and `lon` at [yr.no](https://www.yr.no/en) |
|--- | --- | --- |
| 1. [api.met.no (developer.yr.no: HOWTO)](https://developer.yr.no/doc/locationforecast/HowTO/)<br><br>2. [yr.no](https://www.yr.no/en) | <img width="265" height="177" alt="Image" src="https://github.com/user-attachments/assets/f0f1b728-7384-4e1f-a269-5c378e616914" /> | <img width="1352" height="380" alt="Image" src="https://github.com/user-attachments/assets/128222d7-2cfc-4ad6-be9f-ac86742774f8" /> |

¹ Screenshots were taken about an hour apart, that's why the temperature is slightly higher in the example




## Sources
1. [userbase.kde.org - KDE UserBase wiki](https://userbase.kde.org/KDE_Connect/Tutorials/Useful_commands)
1. [Guilherme (GuinuxBR)](https://github.com/guinuxbr/KDEConnect-commands/blob/main/commands.md)

<br>

# Table of contents
| Title | payload action |
|---|---|
| [Find *your* qdbus command](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-your-qdbus-command) |
| [Sound (PC / System)](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#sound-pc--system-qdbus) | `qdbus` |
| [Media Controls](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#media-controls-qdbus) | `qdbus` |
| [Power management - Screen](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#power-management---screen) | `qdbus` |
| [Power management - Computer](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#power-management---computer) | `qdbus` |
| [Power management - Keyboard](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#power-management---keyboard-lights) | `qdbus` |
| [Find available devices using `kdeconnect-cli`](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#find-available-devices-using-kdeconnect-cli) |
| [Screenshot to device / phone](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#screenshot-to-device--phone) | `kdeconnect-cli --share`  |
| [Weather ping](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/blob/main/README.md#weather-ping---specify-name-like-above) | `kdeconnect-cli --ping-msg` |

###### [Back to top](https://github.com/Skrimpton/KDE-Connect-command-examples-for-Run-Command/edit/main/README.md#table-of-contents)
