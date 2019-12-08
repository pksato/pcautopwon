Small circuit using 555 timer to poweron a computer without option on BIOS to manage poweron behavior, in case of power loss.
Have three conection:
1) 5VSB to power circuit direct from PSU.
2) 5V to detect if main PSU is on.
3) Connection to main board power on switch header.
The 555 is configured as astable oscillator, generating a sort ~1s low pulse every ~10s. This pulse lit the optocouple led and close the transitor, simulating push of the power button.  When power is on (presence of 5V), transistor Q1 saturated, pulling down reset pin of 555, and avoiding the optocouple led to lit. On reset condiction, output pin of 555 goes do low.
The circuit are build on top of PCB (as SMT), to easy fix the board inside the PC case.

Eagle cad files and PNG images.
