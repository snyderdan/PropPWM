PropPWM
=======
PropPWM is a software PWM driver for the Parallax Propeller microcontroller, providing 32-bit PWM to all 32 I/O pins on the prop. This can be used to drive motors, servos, LEDs, etc.
The method used to generate the PWM signals causes an uneven duty cycle, so this is not appropriate for devices expecting a certain duty cycle frequency, as it can range from 75 kHz to .00003 Hz (Setting value to 1 out of 2^32). But this method
provides a much smoother signal as it does not rely on a time proportion. Your duty cycle time is defined by the switching rate instead of the amount of time it takes the processor to iterate 2^x times. 
