# 3D Box Stacking

A 3D game played with your hands and body through the webcam. Walk around the room, pick up the boxes with both hands and stack them in the build zone exactly like the see-through plan shows.

## How to play

- **Lift:** put one hand on each side of a box and bring them together.
- **Carry:** the box sits between your hands and follows them. Tilt your hands to tilt it.
- **Depth:** hands closer to the camera bring the box nearer, further away pushes it deeper. Leaning in to walk doesn't move the box, only your hands do.
- **Put down:** move your hands apart. Over a glowing spot in the plan it clicks into place.
- **Walk:** lean left or right to turn, lean in to walk forward, lean back to walk back. You can't walk through boxes.
- **Re-centre:** if you shift in your seat and start drifting, hold both hands up at the top of the picture for a moment (or press R, or tap 🧍 Re-centre).
- **Pause:** ❚❚ at the top, or P / Esc. The game also pauses when you switch to another window. 🔊 / M turns the sound off.

Each spot in the plan wants a box with a specific letter, and the layer underneath has to be filled first. A box dropped on a spot that wants a different letter is moved out of the build zone so it can't block anything. A box hanging too far over the edge of the box under it slides off.

When none of the boxes you still need are on screen, a yellow arrow at the edge points to the nearest one.

New players can start with the **tutorial**: one box, step by step (show your hands, turn, lift, walk, put down).

Six plans, in order: Wall, Tower, Pyramid, L-shape, Cube and Big pyramid. Later plans have spare boxes that aren't in the plan, so you have to pick the right letters. Your best time for each plan is saved on your device (separately for camera and mouse), and **Next plan** on the win screen takes you to the next one.

No camera? Choose **Play with mouse / touch**: hold to carry, W A S D or the arrow keys to walk and turn, mouse wheel or Q / E for depth. On a phone, use the on-screen arrows and the **Push away / Pull near** buttons.

## Running it

It is one file, `index.html`. The camera only works when the page is opened from a web address (for example GitHub Pages) or from localhost, in Chrome or Edge on a laptop.

## Changing it

The settings are at the top of the script in `index.html`:

- `LEVELS`: the plans, in the order they are played. Each entry in `layers` is one layer, bottom layer first. A layer is either one row of letters, `['A', 'B', 'C']`, or several rows front to back, `[['A', 'B'], ['C', '.']]`, where `.` means no box. `extra` is the number of spare boxes.
- `TUTORIAL`: the tutorial's plan.
- `HOLD_CLOSE` / `HOLD_OPEN`: how close together your hands must be to hold a box, and how far apart to let go.
- `LEAN_...`: how far you have to lean to turn and walk.
- `RECENTRE_HOLD`: how long both hands must be up to re-centre.

## Privacy

Everything runs on your device. The camera picture is never recorded or sent anywhere. Only your hands' outline is shown on screen. The camera is switched off when you go back to the menu. Best times and the sound setting are stored in your browser only.

Hand and face tracking use MediaPipe, and the 3D room uses three.js.
