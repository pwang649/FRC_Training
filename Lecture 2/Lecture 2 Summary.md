# Lecture 2 Summary

The recording is [here](https://youtu.be/PlF1ibXLxmc).

1. We chatted about the overall software architecture and how the program gets executed from a top-down perspective. 
    1. `/lib` contains 3rd party libraries and `/main` contains our source code
    2. Robot.java is the top-level file to be executed
        1. `init()` runs once at the start of the Robot/Auto/Teleop process
        2. `periodic()` runs iteratively after `init()` during Auto/Teoleop until the end of the process
    3. Constants.java contains set constants and parameters such as deviceId, PID constants, and autonomous parameters
2. Next, We moved on to the backbone / mid-level of the software, namely the Subsystems
    4. The purpose of a subsystem class is to bridge the higher-level abstract function call with the lower-level hardware interface
        3. Ex. the Intake subsystem takes in a function call `intake()` and translates that command into steps and output values for the motor hardware
    5. Please understand how the code works for the Intake and the Drive subsystem in our 2019 code
