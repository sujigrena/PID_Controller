# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

We are implementing the very basic and frequently used controller in industry which is the propotional, intergal and differencial control. The error we consider is the Cross Track Error(CTE) which is the difference between the cars orientation and the actual planned path ( with reference to a line).

#### Proportional Control:

The proportional control will steer the car directly proportional to the CTE. This will help us reduce the error and the proportionality between the CTE .The Steer value is determined by the proportionality constant Kp. Note that higher Kp will steer to a greater extent, and could cause the car to oscillate more and make the car to overshoot and takes time to minimize the CTE.

#### Integral Control:

As the name suggests, the Integral control will steer the car proportional to all the errors in the past, i.e it considers the sum of all the past CTE and then take a corrective action. The amount of corrective action depends on the constant Ki. The significance of Integral control is that it helps to overcome the system bias or system error and reach the target point in a smooth way but if the Ki is too large it could lead to oscillations.

#### Differential Control:

The Control action of this control depends on the derivative of the errors, i.e., it considers the change of error to take corrective action. The proportionality is determined by constant Kd. Differential controller help to reduce oscillation but when the Kd is very low the oscillation becomes very large.

#### Final Hyperparameters:
The final values I choose for Kp,Ki and Kd are as follows:

Kp = 0.1 Ki = 0.01 Kd = 2

I manual tweaked each value and observed the output before settling on this value. While trying different value I found for a PID control the Kp acts well in the range 0.05 - .02 when Ki is of the range 0.001 - 0.01 and the Kd is of the range 1-2.

Personally I found these value to run better than other values on my system and hence left them at 0.1,0.01 and 2. I used my understanding and intuition to tweak the values.

