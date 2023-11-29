# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.

Developed by: NIVETHA . S

RegisterNumber:  23002894

Code:

Up counter:

![UPCOUNTER CODE](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/c5bd54ff-848c-4b51-93d8-134844af82a2)

Down counter:

![DOWNCOUNTER CODE - Copy (2)](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/1cb76eaa-4828-4cfa-9778-c33437bac43c)

Time table:

Down counter:

![DOWN TT](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/ba91dcf4-1c00-459a-bee9-0016533923ee)

Up counter:

![UP TT TABLE](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/02e218f4-2939-41b8-823e-764c0d977274)

RTL Diagram:

Down counter:

![DOWNCOUNTER RTL - Copy](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/d011c5ef-60e4-490e-9506-0604f57b961c)

Up counter:

![UPCOUNTER RTL](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/1d312a15-f137-4572-9984-c56548f36b9e)

Output:

Down counter:

![THE REAL DOWN TIME](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/674f290e-3a02-49b5-bf98-fd51f2c91c05)

Up counter:

![UP TIME](https://github.com/nivethasuresh1408/Exp-7-Synchornous-counters-/assets/152055927/f0692f9f-ae22-4587-bc81-f1528c7f541a)





### RESULTS 
