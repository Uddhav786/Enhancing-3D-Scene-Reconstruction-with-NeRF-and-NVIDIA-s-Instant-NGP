# Enhancing-3D-Scene-Reconstruction-with-NeRF-and-NVIDIA-s-Instant-NGP









https://github.com/Uddhav786/Enhancing-3D-Scene-Reconstruction-with-NeRF-and-NVIDIA-s-Instant-NGP/assets/129681467/5986c55e-6518-44c1-b8c8-0a6fe6bbef54

Keyboard shortcuts and recommended controls
Here are the main keyboard controls for the instant-ngp application.

Key	Meaning
WASD	Forward / pan left / backward / pan right.
Spacebar / C	Move up / down.
= or + / - or _	Increase / decrease camera velocity (first person mode) or zoom in / out (third person mode).
E / Shift+E	Increase / decrease exposure.
Tab	Toggle menu visibility.
T	Toggle training. After around two minutes training tends to settle down, so can be toggled off.
{ }	Go to the first/last training image camera view.
[ ]	Go to the previous/next training image camera view.
R	Reload network from file.
Shift+R	Reset camera.
O	Toggle visualization or accumulated error map.
G	Toggle visualization of the ground truth.
M	Toggle multi-view visualization of layers of the neural model. See the paper's video for a little more explanation.
, / .	Shows the previous / next visualized layer; hit M to escape.
1-8	Switches among various render modes, with 2 being the standard one. You can see the list of render mode names in the control interface.
There are many controls in the instant-ngp GUI. First, note that this GUI can be moved and resized, as can the "Camera path" GUI (which first must be expanded to be used).

Recommended user controls in instant-ngp are:

Snapshot: use "Save" to save the trained NeRF, "Load" to reload.
Rendering -> DLSS: toggling this on and setting "DLSS sharpening" to 1.0 can often improve rendering quality.
Rendering -> Crop size: trim back the surrounding environment to focus on the model. "Crop aabb" lets you move the center of the volume of interest and fine tune. See more about this feature in our NeRF training & dataset tips.
The "Camera path" GUI lets you create a camera path for rendering a video. The button "Add from cam" inserts keyframes from the current perspective. Then, you can render a video .mp4 of your camera path or export the keyframes to a .json file. There is a bit more information about the GUI in this post and in this video guide to creating your own video.

VR controls
To view the neural graphics primitive in VR, first start your VR runtime. This will most likely be either

OculusVR if you have an Oculus Rift or Meta Quest (with link cable) headset, and
SteamVR if you have another headset.
Any OpenXR-compatible runtime will work.
Then, press the Connect to VR/AR headset button in the instant-ngp GUI and put on your headset. Before entering VR, we strongly recommend that you first finish training (press "Stop training") or load a pre-trained snapshot for maximum performance.

In VR, you have the following controls.

Control	Meaning
Left stick / trackpad	Move
Right stick / trackpad	Turn camera
Press stick / trackpad	Erase NeRF around the hand
Grab (one-handed)	Drag neural graphics primitive
Grab (two-handed)	Rotate and zoom (like pinch-to-zoom on a smartphone)
