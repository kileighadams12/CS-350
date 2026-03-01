# CS-350

# Project Overview
For this project I built a prototype of a smart thermostat using a Raspberry Pi and several hardware components. The idea was to simulate the basic functionality of a thermostat before adding anything like networking or remote access. The system reads the room temperature from an AHT20 temperature sensor and compares it to a temperature set point that the user controls.

The thermostat has three modes: off, heating, and cooling. One button cycles between those states, and two other buttons allow the user to increase or decrease the temperature set point. LEDs are used to represent what the system is doing. When heating is active and the temperature is below the set point, the red LED fades in and out. When cooling is active and the temperature is above the set point, the blue LED fades. If the temperature reaches the set point, the LED stays solid instead of fading. Overall the project demonstrates how software can control hardware components through GPIO pins while responding to real-time input from sensors and buttons.

# What I Did Well
One thing I think I handled well in this project was organizing the logic using a state machine. Instead of writing a bunch of disconnected conditionals, breaking the system into defined states made it much easier to think through how the thermostat should behave. Each state had clear rules for what should happen when buttons were pressed or when the temperature changed. I also spent time testing each part of the circuit as I built it. Working with hardware means things don’t always behave the way you expect on the first try, so making sure each button, LED, and sensor reading worked correctly helped avoid bigger problems later.

# Where I Could Improve
If I were to revisit this project, I would probably restructure parts of the Python code to make it cleaner. Right now it works, but some sections could be broken into separate functions to make the program easier to read and maintain. I could also improve the documentation. While there are comments explaining parts of the code, adding clearer explanations for how the system flows would make it easier for someone else to understand the project quickly.

# Tools and Resources I Added to My Support Network
Throughout this project I relied heavily on the Raspberry Pi documentation and Python resources when working with GPIO pins and sensors. Community forums and troubleshooting guides were also useful when I ran into issues with button interrupts or sensor readings. Going through this process helped me become more comfortable using technical documentation as a primary resource instead of relying only on examples.

# Transferable Skills
Several things from this project will carry over into future coursework and development projects. Designing and implementing a state machine is something that applies to many different systems, especially when software has to react to user input and environmental conditions. I also gained experience working with event-driven programming and hardware interfaces, which are important skills when working with embedded systems.

# Maintainability, Readability, and Adaptability
To keep the system manageable, I structured the program around clear thermostat states and transitions. That approach makes the system easier to follow because the behavior of the thermostat is tied directly to the current state. I also tried to use clear variable names and comments so the purpose of each part of the code is easier to understand. Because the system logic is organized around a state machine, the design could be extended later to include features like Wi-Fi connectivity or remote monitoring without completely rewriting the program.
