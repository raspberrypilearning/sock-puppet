## Make a buzz

Get the buzzer working 
If you have a microbit V2 you can use the internal buzzer with code XXX ADD BELOW?

do the if NOT thing

--- task ---
Attach short leg to GND

Attach longer led to O

![ALT TEXT](images/circuit-3.png)
--- /task ---


```microbit
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1)) && Mouth_open == false) {
        music.play(music.tonePlayable(880, music.beat(BeatFraction.Half)), music.PlaybackMode.UntilDone)
        music.play(music.tonePlayable(988, music.beat(BeatFraction.Quarter)), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Square)
        Mouth_open = true
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        music.stopAllSounds()
        basic.showIcon(IconNames.SmallSquare)
        Mouth_open = false
    }
})
```

Version 2 only
```microbit
let Mouth_open = true
music.setBuiltInSpeakerEnabled(true)
```

```microbit
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1)) && Mouth_open == false) {
        music.play(music.createSoundExpression(WaveShape.Sawtooth, 4729, 1459, 255, 161, 200, SoundExpressionEffect.Warble, InterpolationCurve.Curve), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Square)
        Mouth_open = true
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        music.stopAllSounds()
        basic.showIcon(IconNames.SmallSquare)
        Mouth_open = false
    }
})
```

