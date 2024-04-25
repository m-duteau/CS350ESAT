# CS350ESAT
The provided files contain code developed and used in the Emerging System Architectures & Designs course module. Both .c files contain code that is meant to run on a TI CC3220S-LAUNCHXL microcontroller.

## Summarize the project and what problem it was solving.
The uartecho.c file contains code that modifies the on/off state of the mcu's LED lights by utilizing a state machine that interprets user input. When the user types "on" in the terminal, the LED will turn on, and when the user types "off", the LED will turn off. This is a basic exercise that demonstrates the ability to comprehend how state machines function and how they can influence the behavior of the mcu.

The gpiointerrupt.c file contains code that runs the mcu as a prototype thermometer. The program utilizes the temperature recognition capabilities embedded in the mcu, and uses the ambient room temperature to determine the heat mode (on/off) based on the setpoint that is set by the user. The "heat" will turn on once the setpoint is greater than the ambient temperature, or the ambient temperature becomes less than the setpoint. The LED light indicates whether heat mode is on or off by the LED staying on when the heat mode is in the "on" state, and the LED light turns off when in the "off" heat state. This program uses a primitive task scheduler-like architecture in order to determine when certain actions take place within the program.

## What did you do particularly well?
Both files demonstrate the capability of controlling the behaviors of a microcontroller by writing code to determine how the microcontroller will function. Both files demonstrated exemplary proficiency based on the assignments' requirements and graded rubrics. 

## Where could you improve?
For gpiointerrupt.c in particular, the task scheduler could have been implemented in a more efficient manner by using a struct that defines the variables of a task and then storing each task in an array so as to run the tasks through a for loop rather than defining each task in main. State machines could also have been implemented to better define and apply the different states required for the tasks' designated functions.

## What tools and/or resources are you adding to your support network?
This is my first experience using code to power a device rather than a program. Consequently, I'm becoming more flexible in my understanding of how code applies to different architectures and how these applications translate into real world scenarios.

## What skills from this project will be particularly transferable to other projects and/or course work?
These projects further built upon my depth of knowledge within the C language family and also provided a starting point within the realm of applying code to devices outside of a computer.

## How did you make this project maintainable, readable, and adaptable?
These projects were made with such elements in mind by the use of good coding practices and utilizing comments effectively in order to benefit other developers' understanding of it should they be required to analyze it. The use of a state machine in uartecho.c also provides a good baseline that would allow for easy implementation of other typed messages to be used for controlling the mcu's behavior.
