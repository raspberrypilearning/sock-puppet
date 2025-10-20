## Foil switch

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Make a foil switch and add to the micro:bit 
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

Open the MakeCode editor at [makecode.microbit.org](https://makecode.microbit.org){:target="_blank"}.

--- /task ---

New to micro:bit?
[[[makecode-tour]]]

--- task ---
### Create your project

Create and name your project: 

Click on the **New Project** button.

<img src="images/new-project-button.png" alt="The New Project button inside MakeCode." width="250"/>

--- /task ---

--- task ---

Give your new project a name (e.g. 'Sock puppet') and click **Create**.

--- /task ---

--- task ---
### Attach foil switch

The puppet uses a foil switch to detect if the mouth is open or closed.

On the micro:bit, clip one bit of foil to `GND` and the other to `P1`{:class='microbitinput'}

![ALT TEXT](images/circuit-4.png)
--- /task ---

--- task ---
Plug your micro:bit into your computer. 

Click download, and the pair button.
--- /task ---

--- task ---
### Add blocks

Drag an `if true`{:class='microbitlogic'} block from the `logic`{:class='microbitlogic'}  menu into the `forever`{:class="microbitbasic"} block.

```microbit
basic.forever(function () {
    if (true) {
    	
    }
})
```
--- /task ---

--- task ---
Drag an `Pin is pressed`{:class='microbitinput'} block over `true`{:class='microbitlogic'}, and change to `P1`{:class='microbitinput'} in the dropdown menu.

![ALT TEXT](images/pressed.gif)
--- /task ---

--- task ---
Add a `show icon`{:class="microbitbasic"}, and choose small square from the menu. 

If the two bits of foil are pressed together, the icon shows.

![ALT TEXT](images/icon.gif)

--- /task ---

--- task ---
To track when the mouth is open and closed make a new `variable`{:class='microbitvariable'} called 'Mouth closed'.

Add a `set Mouth closed`{:class='microbitvariable'} block, and from the `logic`{:class='microbitlogic'} menu add a `true`{:class='microbitlogic'} block.

```microbit
let Mouth_closed = false
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        basic.showIcon(IconNames.SmallSquare)
        Mouth_closed = true
    }
})
```
--- /task ---

--- task ---
**Test:** hold the two foil bits together and see the icon light up.

--- /task ---

--- task ---
### Use a `not`{:class='microbitlogic'}

When the puppet mouth is open, the foil is seperated, and `not`{:class='microbitlogic'} pressed.

In a new `if`{:class='microbitlogic'} block and drag a `not`{:class='microbitlogic'}

```microbit
let Mouth_closed = false
basic.forever(function () {
    if (!(false)) {
    	
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        basic.showIcon(IconNames.SmallSquare)
        Mouth_closed = true
    }
})
```
--- /task ---

--- task ---
Add a `Pin is pressed`{:class='microbitinput'} block, and change to `P1`{:class='microbitinput'}. 

```microbit
let Mouth_closed = false
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1))) {
    	
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        basic.showIcon(IconNames.SmallSquare)
        Mouth_closed = true
    }
})
```
--- /task ---

--- task ---
Add a large square icon from the `basic`{:class='microbitbasic'} menu
```microbit
let Mouth_closed = false
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1))) {
        basic.showIcon(IconNames.Square)
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        basic.showIcon(IconNames.SmallSquare)
        Mouth_closed = true
    }
})

```
--- /task ---

--- task ---
Keep track of when the mouth is open or closed by adding `set Mouth closed`{:class='microbitvariable'} as `false`{:class='microbitlogic'}.

```microbit
let Mouth_closed = false
basic.forever(function () {
    if (!(input.pinIsPressed(TouchPin.P1))) {
        basic.showIcon(IconNames.Square)
        Mouth_closed = false
    }
    if (input.pinIsPressed(TouchPin.P1)) {
        basic.showIcon(IconNames.SmallSquare)
        Mouth_closed = true
    }
})
```
--- /task ---


--- task ---
In the `on start`{:class='microbitbasic'} block add `set Mouth closed`{:class='microbitvariables'} as `true`{:class='microbitlogic'} so that the puppet mouth is closed when starting up.

```microbit
let Mouth_closed = true
```
--- /task ---


--- task ---
**Test:** see the icon light up differently when the foil is pressed or not pressed.
--- /task ---