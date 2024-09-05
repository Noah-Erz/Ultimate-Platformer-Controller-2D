README for info on how to use.
Necessary Child Nodes
These nodes must be attached as a child of the CharacterBody2D node for it to function properly.

Max Speed (float)
The max speed your player will move.

Time to Reach Max Speed (float)
How fast your player will reach max speed from rest.

Time to Reach Zero Speed (float)
How fast your player will reach zero speed from max speed.

Directional Snap (bool)
If true, the player will instantly move and switch directions.

Running Modifier (bool)
If enabled, the default movement speed will by 1/2 of the maxSpeed and the player must hold a "run" button to accelerate to max speed. Assign "run" (case sensitive) in the project input settings.

Jump Height (float)
The peak height of your player's jump.

Jumps (int)
How many jumps your character can do before needing to touch the ground again. Giving more than 1 jump disables jump buffering and coyote time.

Gravity Scale (float)
The strength at which your character will be pulled to the ground.

Terminal Velocity (float)
The fastest your player can fall.

Descending Gravity Factor (float)
Your player will move this amount faster when falling providing a less floaty jump curve.

Short Hop AKA Variable Jump Height (bool)
Enabling this toggle makes it so that when the player releases the jump key while still ascending, their vertical velocity will cut in half, providing variable jump height.

Coyote Time (float)
How much extra time (in seconds) your player will be given to jump after falling off an edge. This is set to 0.2 seconds by default.

Jump Buffering (float)
The window of time (in seconds) that your player can press the jump button before hitting the ground and still have their input registered as a jump. This is set to 0.2 seconds by default.

Wall Jump (bool)
Allows your player to jump off of walls. Without a Wall Kick Angle, the player will be able to scale the wall.

Input Pause After Wall Jump (float)
How long the player's movement input will be ignored after wall jumping.

Wall Kick Angle (float)
The angle at which your player will jump away from the wall. 0 is straight away from the wall, 90 is straight up. Does not account for gravity

Wall Sliding (float)
The player's gravity will be divided by this number when touch a wall and descending. Set to 1 by default meaning no change will be made to the gravity and there is effectively no wall sliding. 
THIS IS OVERRIDDED BY WALL LATCH.

Wall Latching (bool)
If enabled, the player's gravity will be set to 0 when touching a wall and descending. THIS WILL OVERRIDE WALLSLIDING.

Wall Latching Modifier (bool)
Wall latching must be enabled for this to work. #If enabled, the player must hold down the "latch" key to wall latch. Assign "latch" in the project input settings. The player's input will be 
ignored when latching.

Dash Type (enum)
Types -
2 Way Horizontal
2 Way Vertical
4 Way Cardinal
8 Way Cardinal
The type of dashes the player can do.

Dashes (int)
How many dashes your player can do before needing to hit the ground.

Dash Cancel (bool)
If enabled, pressing the opposite direction of a dash, during a dash, will zero the player's velocity.

Dash Length (float)
How far the player will dash. One of the dashing toggles must be on for this to be used.

Corner Cutting (bool)
If the player's head is blocked by a jump but only by a little, the player will be nudged in the right direction and their jump will execute as intended. NEEDS RAYCASTS TO BE ATTACHED TO THE 
PLAYER NODE. AND ASSIGNED TO MOUNTING RAYCAST. DISTANCE OF MOUNTING DETERMINED BY PLACEMENT OF RAYCAST.

Correction Amount (float)
How many pixels the player will be pushed (per frame) if corner cutting is needed to correct a jump.

Left Raycast (Raycast2D)
Middle Raycast (Raycast2D)
Right Raycast (Raycast2D)
Raycast used for corner cutting calculations. ALL ARE NEEDED FOR IT TO WORK.

Crouch (bool)
Holding down will crouch the player. Crouching script may need to be changed depending on how your player's size proportions are. It is built for 32x player's sprites.

Can Roll (bool)
Holding down and pressing the input for "roll" will execute a roll if the player is grounded. Assign a "roll" input in project settings input.

Roll Length (float)
The length of the roll.

Ground Pound (bool)
If enabled, the player will stop all horizontal movement midair, wait (groundPoundPause) seconds, and then slam down into the ground when down is pressed. 

Ground Pound Pause (float)
The amount of time the player will hover in the air before completing a ground pound (in seconds).

Up to Cancel
If enabled, pressing up will end the ground pound early.

Animations (all bools)
run
jump
idle
walk
slide
latch
falling
crouch_idle
crouch_walk
roll 
Animations must be named "name" all lowercase as the check box says.
Looping Animations:
run, walk, idle, crouch_idle, crouch_walk
Non-looping Animations:
jump, slide, roll
Single Frame Sprites Frames:
Latch, falling
