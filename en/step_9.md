## Rotate 


add cable (need to make image) also is the final image of the whole thing togheter

--- task ---

look at accelerometer data in the serial port
--- /task ---

```microbit
let puppet_talking = true
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1)) && puppet_talking == false) {
        if (input.rotation(Rotation.Pitch) < -40) {
            CuteSounds.play(CuteSounds.Sound.HAPPY)
            puppet_talking = true
        } else {
            CuteSounds.play(CuteSounds.Sound.SAD)
            puppet_talking = true
        }
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        music.stopAllSounds()
        puppet_talking = false
    }
    serial.writeValue("rotation", input.rotation(Rotation.Pitch))
})
```

