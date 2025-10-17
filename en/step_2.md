## Foil switch
Get switch working for a basic 

--- task ---

Open the sarter project ADD LINK

--- /task ---

New to micro:bit?
[[[makecode-tour]]]

--- task ---
Attach one of the foil pieces to GND

Attach the other to 1

![ALT TEXT](images/circuit-4.png)
--- /task ---


```microbit
let puppet_talking = true
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1)) && puppet_talking == false) {
        basic.showIcon(IconNames.Heart)
        puppet_talking = true
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        puppet_talking = false
    }
})

```
