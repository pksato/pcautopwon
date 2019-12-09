Small circuit using 555 timer to poweron a computer without option on BIOS to manage poweron behavior, in case of power loss. 
  
Its have three connection:  
5VSB to power circuit direct from PSU.  
5V to detect if main PSU is on.  
Connection to main board power on switch header.  
          
The 555 is configured as astable oscillator, generating a sort ~1s low pulse every ~10s. This pulse lit the optocoupler led and close the transistor, simulating push of the power button. When power is on (presence of 5V), transistor Q1 saturate, pulling down reset pin of 555, and avoiding the optocoupler led to lit. On reset condition, output pin of 555 goes do low. The circuit are build on top of PCB (as SMT), to easy fix the board inside the PC case.
  
EagleCad files and PNG images.
  
OBS.:
The mainboard where this circuit is used don't have option on BIOS to manage power state when mains AC return. And power on when power switch is released. Also, have a delay after mains applied and able to press power button.
