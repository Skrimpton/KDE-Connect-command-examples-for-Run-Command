# KDE-Connect-command-examples-for-Run-Command
It's KDE Connect command examples for "Run Command"

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

#### Media - Next Track
```
qdbus6 org.kde.keyboard /component/mediacontrol org.kde.kglobalaccel.Component.invokeShortcut nextmedia
```

#### Media - Previous Track
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
