---
layout: default
category: Advanced Robot Tutorials
order: 1
title: Tuning PIDs
---
## Velocity/Motion Profiling (CTRE Phoenix)

1. Calculate Feedforward Gain (F)
    1. Power motor with 100% power
    2. Self-test the TalonSRX on roboRIO dashboard
    3. Look for velocity reading of encoder and plug the velocity into the following equation:
        * F = (MotorOutput% * 1023) / Velocity
        * 1023 = Full forward power on motor
        * Motor Output % = Amount of power you're supplying motor
        * Velocity is the velocity you found when using the TalonSRX self-test
2. Calculate Proportional Gain (P)
    1. Print out closed loop error with just the F-Gain inputted and the rest of the constants set to 0.
    2. Run the motor
    3. Find the largest error of the closed loop
    4. Plug largest error into the following equation:
        * P = (MotorOutputResponse% * 1023) / LargestError
        * Motor Output Response % = The output % you want to supply the motor when there's an error in the closed loop. (Usually we'll just supply 10%) Ex: When we see the LargestError from the loop it will supply the motor 10% more power in order to correct itself to decrease the error.
        * 1023 = Full forward power on motor
        * LargestError = The largest error that you found within the closed loop with only the F-Gain set.
    5. Double the output of the equation until the motor oscillates (Motor will start going back and forth rapidly).
    6. Once it oscillates go back to the output previous and add small increments until the error is as close to your desired setpoint.

3. Usually the I and D Gain aren't really needed but if you really need just a little bit more to reach no error you can start with the D-Gain
    1. If the motor is moving a little too fast at the start add the D-Gain to smooth the motion. Start with 10x the P-Gain and increase or decrease accordingly.
    2. If the motor is still not quite reaching the setpoint use the I-Gain. I-Gain usually starts at 1/100th of the P-Gain and increase or decrease accordingly.

## Position

1. Zero out all the values.
2. Find the setpoint you want to get to (The sensor value you want to get to. We'll use an encoder mounted on the elevator for this example).
    1. If we wanted to have the setpoint as the middle of the elevator move the elevator by hand to the middle position and hold it there.
    2. Self-test the TalonSRX on the roboRIO dashboard.
    3. Record the position the encoder is at (Make sure the sensor is in phase a.k.a when you move the motor in the positive direction the sensor moves in the positive direction also).
3. Make sure the elevator is under load (is carrying the game piece).
4. Start with the Proportional Gain (P)
    1. Set the P to 1
    2. Run the elevator and input the setpoint and print out the closed-loop error.
    3. If the error is positive then it needs more power to make it not undershoot the setpoint usually you'll just add a decimal point to the current value. Ex: It's currently 1 then increase to 1.1 and repeat until the error is too large when you go up a decimal point.
    4. If the error is negative then it needs less power to make it not overshoot the setpoint usually you'll just go down a decimal point from the current value. Ex: It's currently 1 then decrease to 0.1 and repeat until the error is too large when you go down a decimal point
    5. Once you found the decimal point you need to be at start adding to the current value (I usually go by halves). Ex: It's currently at 0.01 then change it to 0.05 and see what happens. If it's too much then half it to 0.025. If it's too little then add a quarter like from 0.05 to 0.75 and repeat.
5. If the elevator accelerates too quickly then add a Derivative Gain (D).
    * Usually you'll start at 10x to 100x of the current P value and increase/decrease accordingly.
6. If the elevator never quite reaches the setpoint then add a Integral Gain (I).
    * Usually you'll start at 1/100th of the P value and increase/decrease accordingly.
