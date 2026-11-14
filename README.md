# 3D Box Stacking

A 3D game played with your hands and body through the webcam. Walk around the room, pick up the boxes with both hands and stack them in the build zone exactly like the see-through plan shows.

## How to play

- **Lift:** put one hand on each side of a box and bring them together.
- **Carry:** the box sits between your hands and follows them. Tilt your hands to tilt it.
- **Depth:** hands closer to the camera bring the box nearer, further away pushes it deeper.
- **Put down:** move your hands apart. Over a glowing spot in the plan it clicks into place.
- **Walk:** lean left or right to turn, lean in to walk forward, lean back to walk back.
- **Re-centre:** tap this at the top if you shift in your seat and start drifting.

Each spot in the plan wants a box with a specific letter, and the layer underneath has to be filled first.

Three plans: Wall (6 boxes), Pyramid (6) and Big pyramid (10).

No camera? Choose **Play with mouse / touch**: hold to carry, W A S D or the arrow keys to walk and turn, mouse wheel or Q / E for depth.

## Running it

It is one file, `index.html`. The camera only works when the page is opened from a web address (for example GitHub Pages) or from localhost, in Chrome or Edge on a laptop.

## Changing it

The settings are at the top of the script in `index.html`:

- `LEVELS`: what has to be built. Each line is one layer, bottom layer first.
- `HOLD_CLOSE` / `HOLD_OPEN`: how close together your hands must be to hold a box, and how far apart to let go.
- `LEAN_...`: how far you have to lean to turn and walk.

## Privacy

Everything runs on your device. The camera picture is never recorded or sent anywhere. Only your hands' outline is shown on screen.

Hand and face tracking use MediaPipe, and the 3D room uses three.js.
