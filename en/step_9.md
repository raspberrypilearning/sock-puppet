## Rotate 


add cable (need to make image) also is the final image of the whole thing togheter

--- task ---

look at accelerometer data in the serial port
--- /task ---

```microbit
basic.forever(function () {
    serial.writeValue("rotation", input.rotation(Rotation.Pitch))
})
```

Go to device view
![ALT TEXT](images/rotate-1.png)

look at how the graph moves when you move your arms
![ALT TEXT](images/rotate-2.gif)

record the number when down (in this case it is -38)
![ALT TEXT](images/rotate-3.png)

