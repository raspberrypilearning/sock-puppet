## Make a foil switch

--- task ---
### Open the project

Open the starter project at [rpf.io/sock-puppet](https://rpf.io/sock-puppet){:target="_blank"}.
--- /task ---


--- task ---
### Make a foil switch

The puppet uses a foil switch to detect if the mouth is **open** or **closed**.

![An animation of the foil switch in the puppet's mouth, with the mouth being opened and closed.](images/open-close.gif)

Clip the foil to the micro:bit to create the switch. Connect one piece of foil to **GND** and the other to **pin 1**. When the foil pieces touch, it completes the circuit.

![A diagram of the micro:bit circuit. Two pieces of foil are connected to the micro:bit with crocodile clips.](images/circuit-4.png){:width="500px"}
--- /task ---


--- task ---
### Plug in the board

Connect the micro:bit to your computer with the micro USB cable. 

Click on **Download**, and pair the micro:bit with your computer.

--- /task ---


--- task ---
### Add the input block

Drag an `on pin released`{:class='microbitinput'} block from the `Input...more`{:class='microbitinput'} menu. 

In the drop-down menu, change the pin to `P1`{:class='microbitinput'}.

```microbit
input.onPinReleased(TouchPin.P1, function () {	
})
```
--- /task ---

**Tip:** The `Input...more`{:class='microbitinput'} menu is hidden and will appear when you open the `Input`{:class='microbitinput'} menu.

![An animation of opening the 'Input...more' menu, dragging an 'on pin released' block into the editor, and changing the pin to P1.](images/released.gif){:width="500px"}


--- task ---
Add a `show icon`{:class='microbitbasic'} block from the `Basic`{:class='microbitbasic'} menu. 

Select an icon in the drop-down menu. In this example, we use the square icon.

The icon will appear when the foil switch is open.

```microbit
input.onPinReleased(TouchPin.P1, function () {
    basic.showIcon(IconNames.Square)
})
```
--- /task ---


--- task ---
**Test:** Connect the two pieces of foil together, then release them to see the icon appear.
--- /task ---