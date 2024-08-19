## TinyML

This course is part of the Verizon Skill Forward program. Thank you to Verizon for providing the full course experience for self-learners like me.

### Introduction
* TinyML is concerned with creating intelligent systems on microcontrollers.
* Microcontrollers are cheap, energy efficient, and resource contrained devices.
* Big Picture: Generate predictions from data generated by external sensors (i.e. cameras, pressure, temperature, etc.).

### Hardware and Software Challenges
Hardware | Software 
-|-
Limited in terms of performance, power consumption, and storage | Not as portable as mainstream software

### Floating Point Numbers on Embedded Systems
Before, floating point operations were handled via software libraries, but they were slow. Now, with Floating Point Units (FPUs), which are dedicated hardware processors to perform operations on floating point numbers, operating on floating point numbers are much faster. However, if you write code optimized for a specific FPU, it may not work on other FPUs, as they may have different architectures or instruction sets.

### Embedded Machine Learning Software Challenges
Larger models require more computational power but an embedded systems can only offer so much it. So, we need to find a way to fit these large models into our microcontrollers while keeping the restrictions in mind. Here are some ways of doing so:
* Model Compression: Pruning - Removing some nodes and connections while still producing the same results.
* Model Compression: Quantization - Reducing the size of the numbers we're working with to take up less memory space.
* Model Compression: Knowledge Distillation - Only keep the most critical pieces of information to produce our results.
* Reducing Runtimes: Making inferences from our pre-made model instead of learning from new data