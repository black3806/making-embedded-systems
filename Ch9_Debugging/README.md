# Chapter XX: Debugging
This is a companion repository for _Making Embedded Systems, 2nd Ed._ by Elecia White. 


# Following Along in the Book
[Compiler Explorer](https://godbolt.org/) is a web tool lets you look at the assembly that your code becomes after compilation. In the book, there is an example with an interrupt that needs a volatile. You can see that at Compiler Explorer [here](https://godbolt.org/z/G49oYYevs). If you change the compiler options from -O3 (optimized) to -O0 (unoptimized), the while loop returns to the assembly Alternatively, if you make the `global` variable volatile, the while loop remains because the `volatile` keyword lets the compiler know other piece of code may modify the variable.

[Rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging) is when you explain your issue to an inanimate object. It is surprisingly effective.


## Debugging Hard Faults (Arm Cortex-M)

In [Ending the Embedded Software Dark Ages: Let’s Start With Processor Fault Debugging!](https://embeddedartistry.com/blog/2021/01/11/hard-fault-debugging/), Phillip at Embedded Artistry goes through the whole process of debugging from manually walking through the hardfault to creating good handlers to making a mini-core dump for later use. 

That links to Interrupt Blog’s [How to Debug a Hard Fault on an Arm Cortex-M MCU](https://interrupt.memfault.com/blog/cortex-m-fault-debug) which is the most tactical hands-on resource.

More information about hardfaults
 * [Debugging Hard Faults on ARM Cortex-M | MCU on Eclipse](https://mcuoneclipse.com/2012/11/24/debugging-hard-faults-on-arm-cortex-m/)
 * [STM32 Hard Fault debugging](https://mcuoneclipse.com/2012/11/24/debugging-hard-faults-on-arm-cortex-m/)
 * [FreeRTOS Debugging and diagnosing hard faults on Arm Cortex-M CPUs](https://www.freertos.org/Debugging-Hard-Faults-On-Cortex-M-Microcontrollers.html)


In [Ending the Embedded Software Dark Ages: Let’s Start With Processor Fault Debugging!](https://embeddedartistry.com/blog/2021/01/11/hard-fault-debugging/), Phillip at Embedded Artistry goes through the whole process of debugging from manually walking through the hardfault to creating good handlers to making a mini-coredump for later use.


Arm Documentation: [Configurable Fault Status Register - Cortex-M3](https://developer.arm.com/documentation/dui0552/a/cortex-m3-peripherals/system-control-block/configurable-fault-status-register) 

[Profiling Firmware on Cortex-M](https://interrupt.memfault.com/blog/profiling-firmware-on-cortex-m) from Interrupt provides an code to create a sample Profiling with GBD and awk on a Cortex-M processor. (It also shows other profiling methods.)

## Linker Files
Here is an [excellent and through post about linker files](https://mcyoung.xyz/2021/06/01/linker-script/). I also recommend [The most thoroughly commented linker script (probably)](
)

Miguel Young de la Sota’s post about [Everything You Never Wanted to Know About Linker Script](https://mcyoung.xyz/2021/06/01/linker-script/) is an excellent post about linker files.  
Another great resource is Thea Flowers’ post on [the most thoroughly commented linker script (probably)](https://blog.thea.codes/the-most-thoroughly-commented-linker-script/). Finally, 
Phillip Johnston’s [Linker-Generated Variables in Libc](https://embeddedartistry.com/lesson/linker-generated-variables-in-libc/) shows how to use and set linker variables.


## Memory

[Pointers in C / C++ video on YouTube](https://www.youtube.com/watch?v=zuegQmMdy8M)



# Code For This Chapter

hardfault.c

# Final Note
If you like what's here, please consider buying the book: [_Making Embedded Systems, 2nd Ed._](https://learning.oreilly.com/library/view/making-embedded-systems/9781098151539/) by Elecia White