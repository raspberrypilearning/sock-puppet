## Make some noise

Get the buzzer working 
If you have a microbit V2 you can use the internal buzzer with code XXX ADD BELOW?

do the if NOT thing

--- task ---
Attach short leg to GND

Attach longer led to O

![ALT TEXT](images/circuit-3.png)
--- /task ---

--- task ---

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




--- /task ---