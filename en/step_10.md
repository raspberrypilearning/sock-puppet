## Change sounds on rotate 

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

--- task ---
### View serial data

Add a new `forever`{:class='microbitbasic'} block.

Under `Advanced`, drag a `serial write`{:class='microbitserial'} block.

```microbit
basic.forever(function () {
    serial.writeValue("x", 0)
})
```
--- /task ---


--- task ---
From the `input - more`{:class='microbitinput'} menu drag `rotation`{:class='microbitinput'} into the second field. 

In the first field type 'rotation'.

![ALT TEXT](images/rotation.gif)
--- /task ---


--- task ---
Click on **Show data Device**, you might need to scroll to see it.

![ALT TEXT](images/rotate-1.png) 
--- /task ---


--- task ---
Look at how the rotation data changes when you move the puppet.

![ALT TEXT](images/rotate-2.gif)
--- /task ---


--- task ---
You can see the rotation number below the graph in a list.

Choose a rotation number for when the puppet's head is down. Here it is between -35 and -39, I have chosen -38.

![ALT TEXT](images/rotate-3.png)
--- /task ---
