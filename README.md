This repo is part of a student project for the minor Intelligent Mobility at Rotterdam University of Applied Sciences (Hogeschool Rotterdam).

The original CanFestivino repo this is forked from had, at the time, been inactive for 6 years and was written in the depricated Python version 2, but was the only resource available with an example of CanOpen using Arduino. We made some minor changes in order to get the code working and making it easier to use.

Through a lot of experimentation, we managed to get it working just enough to fit our own specific needs, as completely modernising the code was not within the scope of our project.

After doing this, we noticed that many of our fellow students were also working with CANBUS and wished to try CanOpen for themselves, so we decided to fork the original CanFestival and make our changes available to them and sharing what we have learned so far.

##### If you wish to use our work for your own project, please consult the Installation Guide, which explains the steps necessary to set up a basic CANBUS network between an Arduino with a potentiometer and servo and a Raspberry Pi using some CANBUS modules based on the MCP2515.

> ##### If you are interested in a more actively developed version of CanOpen, maybe take a look at the [open source library from Lely](https://opensource.lely.com/canopen/) (a large Dutch company that develops robots for the agricultural sector). As of writing, they did not have an Arduino-specific example, but with the right know-how, and possibly cross-referencing CanFestival/CanFestivino it could potentially be built for Arduino.

# Original README from fork
> # History from 07/27/2015
> * Extensive changes to reduce SRAM usage
> * Removed need for extra timers
> * Added write access flag to object dict entry callback
> * objdictedit from this repo needed to generate suitable object dictionary definition
> * mcp_can, BlinkPattern, digitalWriteFast and Timer libraries from my repos needed to successfully compile
> * MCP2515 chip select pin set in CO_can_Arduino.cpp
> * Usage: define `CO<red_led_pin, green_led_pin> co;` (-1 if no led needed), call `co.CO_Init();` in `setup()`, call `co.CO_Cycle();` in `loop()`
> * See example
> 
> # History from 11/02/2015
> This is a first working prototype with only the most necessary changes to the original CANFestival code to make it run as an Arduino library.
> 
> [Here](https://github.com/jgeisler0303/AGCON/tree/master/Software/Arduino) is an intermediate state of this library before I started to compile it using the Arduino IDE.
> 
> The example uses [my fork](https://github.com/jgeisler0303/CAN_BUS_Shield) of the [Seeed Studio CAN bus library](https://github.com/Seeed-Studio/CAN_BUS_Shield). Beware that my example expects the CS of the MCP2515 on a different pin than the Seeed CAN bus shield.
> 
> The object dictionary that is implemented by the example must be edited with [my special version](https://github.com/jgeisler0303/AGCON/tree/master/Software/CanFestival/objdictgen) of the CANFestival tool in order to generate code that doesn't conflict with Arduino conventions.
> 
> Further documentation to follow.
