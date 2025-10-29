## Foil switch

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Make a foil switch and add to the micro:bit 
</div>
<div>

![Animated gif of sun moving accross city](images/sun.gif)

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
### Open the project

Open the starter project at [makecode.microbit.org](https://rpf.io/sock-puppet){:target="_blank"}.
--- /task ---


--- task ---
### Make a foil switch

The puppet uses a foil switch to detect if the mouth is **open** or **closed**.

![Animated gif of foil switch in puppet mouth opening and closing](images/open-close.gif)

Clip the foil to the Micro:bit to create the switch. One bit of foil is connected to `GND` and the other to `P1`{:class='microbitinput'}

![Diagram of the microbit circuit - showing a foil switch connceeted with crocodile clips](images/circuit-4.png){:width="500px"}
--- /task ---


--- task ---
### Plug in the board

Plug the Micro:bit into your computer with the USB cable. 

Click download, and pair the Micro:bit with your computer.
--- /task ---


--- task ---
### Add the input block

Drag a `pin released`{:class='microbitinput'} block from the `more input`{:class='microbitinput'} menu. 

In the dropdown menu change the pin to `P1`{:class='microbitinput'}.

```microbit
input.onPinReleased(TouchPin.P1, function () {	
})
```
--- /task ---

**Tip:** The `more input`{:class='microbitinput'} menu is hidden, and will appear when you click on input.

![Animated gif of mircobit menu, showing how to find the more input menu, and dragging pin released into the editor](images/released.gif){:width="500px"}


--- task ---
Add a `show icon`{:class='microbitbasic'} from the `basic`{:class='microbitbasic'} menu

The icon will show when the foil switch is open.

```microbit
input.onPinReleased(TouchPin.P1, function () {
    basic.showIcon(IconNames.Square)
})
```
--- /task ---


--- task ---
**Test:** connect the two foil bits together and see the icon show when they are released.
--- /task ---