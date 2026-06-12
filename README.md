## Description
Our robot used an X-drive wheelbase which cannot be used with integrated Vex-IQ drivebases.
This means that I had to program my own drive system without the use of gyros.
My drivesystem uses functions to define Forwards, Backwards, Left, Right and turns with times instead of distances.
This works well for our usecase as our robot operated in a set map. 
I also made special moves which consist of

- bump: moves the robot left untill the bump sensor detects a wall. (aligns the robot to the left wall)
- moveTillDist: moves the robot forwards untill it detects something
- CLAWOpen: opens claw
- CLAWClose: closes claw
- ARMDown: moves arm down
- ARMUp: moves arm down 

Our code scans for the blocks, strafing against the back wall, then picks them up, aligns itself then deposits the block in the goal.
It repeats this 3 times with varying levels of error detection. Then finishes and plays a sound.
