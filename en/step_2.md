## Rotate 


--- task ---

Open the sarter project ADD LINK

--- /task ---

New to micro:bit?
[[[makecode-tour]]]

--- task ---

look at accelerometer data in the serial port
--- /task ---
basic.forever(function () {
    serial.writeValue("rotation", input.rotation(Rotation.Pitch))


