## Challenge! Sound and gestures
<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Give your puppet more character when it moves.
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
### Add a gesture

Remove the `Play`{:class='microbitfunctions'} block and add an `if else`{:class='microbitlogic'} block from the `logic`{:class='microbitinput'} menu. 

![Microbit blocks - showing the if else block inside a pi released](images/challenge-1.png){:width="400px"}
--- /task ---


--- task ---
👀 Look at which way up your Micro:bit is on the puppet. If the Microbit is facing down, you can use the `logo down gesture`{:class='microbitinput'} block to trigger the sound in the next step.

**Tip:** if the Micro:bit is a differnt way up, experiment with some of the other gestures.

![Showing the Micro:bit on the back of the sock puppet, with an arrow illustraitng how the Micro:bit is facing down](images/down.png){:width="500px"}
--- /task ---




--- task ---
Drag the `logo shake gesture`{:class='microbitinput'} block next to the `if` {:class='microbitlogic'}. 

Choose `logo down`{:class='microbitinput'} from the dropdown menu, or a different gesture that works for your puppet. 

![Animated gif of a Make code gesture input blocks](images/challenge-2.gif){:width="400px"}

--- /task ---

--- task ---
Add the `play HELLO`{:class='microbitfunctions'} block into the top of the `if`{:class='microbitlogic'} block. 

This will play the "hello" sound when the puppet is up.

![Make code gesture input blocks and a play block inside a if](images/challenge-3.png){:width="400px"}

--- /task ---


--- task ---
Add a new `play`{:class='microbitfunctions'} block from the Puppet{:class='microbitfunctions'} menu into the `else`{:class='microbitlogic'} part of the block, and choose the `ohh`{:class='microbitfunctions'} sound.

This will make a sad sound when the puppet is down.

![Make code gesture input blocks and a play block inside a if with another play block in the else](images/challenge-4.png){:width="400px"}

--- /task ---

--- task ---
**Test:** check the sad and happy sounds are working when you rotate the puppet and open the mouth.
--- /task ---

