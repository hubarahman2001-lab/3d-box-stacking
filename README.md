# 3D Box Stacking

A 3D game played with your hands through the webcam. Walk around the room, pick up the boxes with both hands and stack them in the build zone exactly like the see-through plan shows.

**Play:** https://hubarahman2001-lab.github.io/3d-box-stacking/

## How to play

Sit about an arm's length from the laptop so the camera sees both hands.

- **Lift:** point at a box you can reach and two hand outlines appear on its sides. Put your hands there, then squeeze in. Your 3D hands grip the box and it lifts.
- **Carry:** the box goes where you point, over the floor or on top of other boxes. Tilt your hands to tilt it. If the camera loses one hand (they often overlap) you keep hold of the box.
- **Put down:** move your hands apart. Over a glowing spot in the plan it clicks into place. A box in its right place is finished and can't be picked up again by mistake.
- **Walk:** point at a box that's too far away and hold still, or carry a box and hold it over the build zone. A ring fills up and you walk there by yourself.
- **Turn:** put your hands in the **TURN** zones at the left or right edge of the screen.
- **Yellow arrow:** when what you need isn't on screen, a yellow arrow appears at the edge. Hold your hands on it to go to the next box, or, while carrying one, to the spot it goes in.
- **Pause:** ❚❚ at the top, or P / Esc. The game also pauses when you switch to another window. 🔊 / M turns the sound off.

Each spot in the plan wants a box with a specific letter, and the layer underneath has to be filled first. A box dropped on a spot that wants a different letter is moved out of the build zone so it can't block anything. A box hanging too far over the edge of the box under it slides off.

New players can start with the **tutorial**: one box, step by step (show your hands, turn, lift, walk, put down).

Six plans, in order: Wall, Tower, Pyramid, L-shape, Cube and Big pyramid. Later plans have spare boxes that aren't in the plan, so you have to pick the right letters. Your best time for each plan is saved on your device (separately for camera and mouse), and **Next plan** on the win screen takes you to the next one.

No camera? Choose **Play with mouse / touch**: hold on a box to carry it, click a far box (or the yellow arrow) to walk to it, W A S D or the arrow keys to walk and turn. On a phone, use the on-screen arrows.

## Running it

It is one file, `index.html`. The camera only works when the page is opened from a web address (for example GitHub Pages) or from localhost, in Chrome or Edge on a laptop.

## Changing it

The settings are at the top of the script in `index.html`:

- `LEVELS`: the plans, in the order they are played. Each entry in `layers` is one layer, bottom layer first. A layer is either one row of letters, `['A', 'B', 'C']`, or several rows front to back, `[['A', 'B'], ['C', '.']]`, where `.` means no box. `extra` is the number of spare boxes.
- `TUTORIAL`: the tutorial's plan.
- `SQUEEZE`, `GRIP_TIME`, `RELEASE_APART`: how much to squeeze to lift, how long before it lifts, and how far apart to move your hands to put it down.
- `LOST_DROP`: how long the camera can lose both hands before a carried box is put down.
- `DWELL`: how long to hold still to walk somewhere.
- `TURN_EDGE`: how wide the turn zones at the screen edges are.
- `ARM_REACH` / `CARRY_REACH`: how near a box must be to lift it, and how far you can carry it from where you stand.

## Privacy

Everything runs on your device. The camera picture is never recorded or sent anywhere. Only your hands' outline is shown on screen. The camera is switched off when you go back to the menu. Best times and the sound setting are stored in your browser only.

Hand tracking uses MediaPipe, and the 3D room uses three.js.
