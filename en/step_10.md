## Rotate 

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Make a foil switch and add to micro:bit 
</div>
<div>

![Animated gif of sun moving accross city](images/sun.gif){:width="300px"}

</div>
</div>

<html>
<div style="position: relative; width: 100%; aspect-ratio: 16 / 9; border-radius: 20px; box-shadow: 0 0 15px #3fb654; overflow: hidden;">
<iframe style="position: absolute; top: 0; left: 0; right: 0; width: 100%; height: 100%; border: none;" src="https://www.youtube.com/embed/t5UzLuTj_CE?rel=0&cc_load_policy=1" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share">
</iframe>
</div><br>
</html>
<div style="text-align: center; margin-top: 1em;">

Play, pause, make. Follow the project on our [YouTube](10) playlist!
</div>
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

