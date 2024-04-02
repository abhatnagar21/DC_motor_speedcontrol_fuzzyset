# DC_motor_speedcontrol_fuzzyset
Speed control of DC motor using fuzzyset in python

1. PIDController Class:
The PIDController class implements a basic Proportional-Integral-Derivative (PID) controller.
It takes the PID constants (Kp, Ki, Kd), and the setpoint (desired speed) as inputs during initialization.

The update method takes the current value i.e the motor's current speed as input and returns the control output i.e voltage adjustment.

The PID controller keeps track of the previous error (prev_error) and the integral term (integral) to compute the control output.

2. DCMotor Class:
The DCMotor class simulates a DC motor.
It has a method set_voltage to adjust the motor's input voltage based on the control output from the PID controller.
In this example, we simulate motor behavior by adjusting the motor's speed based on the applied voltage.

3. Constants and Initialization:

Constants for the PID controller (Kp, Ki, Kd) and the desired speed (setpoint) are set.
An instance of the PID controller (pid_controller) and the DC motor (dc_motor) are initialized.

4. Simulation Loop:

In the simulation loop, the current speed of the motor is measured 
The PID controller is used to compute the voltage adjustment required to achieve the desired speed.
The computed voltage adjustment is applied to the motor using the set_voltage method.
The loop prints out the desired speed, current speed, and voltage adjustment for each iteration.
A small delay is introduced in each iteration to simulate the motor's response time.

Output:

During each iteration of the loop, the desired speed, current speed, and voltage adjustment are printed to the console.
This allows us to observe how the PID controller adjusts the voltage to control the motor's speed towards the desired setpoint.
