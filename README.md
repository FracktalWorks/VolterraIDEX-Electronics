# VolterraIDEX-Electronics
Pin Configurations, EagleCAD and gerber files for Volterra IDEX PCBs

The following documentation contains the contents about the pin connections, firmware configurations of the BigTreeTech Octopus V1.1 which is assembled into the VolterraIDEX model of 400x400x370 buildsize.

## Initial Preparation
set jumpers as shown:
![image](https://user-images.githubusercontent.com/80109965/224631780-a06c66a4-45b7-4c35-9ae4-ff0ac69d6ade.png)

Green – Add Jumper

Red – Remove Jumper

1. Insert only the jumper in the Green and remove the other three jumpers in the Red in order to use TMC2209 UART mode.
2. Remove all the jumpers of DIAG to avoid the influence of TMC2209 DIAG on the endstop.
3. Remove the USB 5V power supply jumper to avoid the interaction between the USB 5V of raspberry pi and the DC-DC 5V of the motherboard.
4. Insert all the jumpers into V_FUSED to set the fan voltage to the system supply voltage.
5. Insert the jumper into V_FUSED to set the probe voltage to the system supply voltage.

## Wiring
1. Connect 24V and GND (V+ and V-) from the PSU to PWR and MOTOR_POWER
2. Connect the X(L) Motor (gantry left) to MOTOR0
3. Connect the X(R) Motor (gantry right) to MOTOR1 
4. Connect the E0 (Left Extruder front) motor to MOTOR2_1
5. Connect the E0' (Left Extruder back) motor to MOTOR2_2
6. Connect the Z motor to MOTOR3
7. Connect the Y (gantry left) to MOTOR4
8. Connect the Y1 (gantry right) to MOTOR5
9. Connect the E1 (Right Extruder front) to MOTOR6
10. Connect the E1' (Right Extruder back) to MOTOR7
11. Connect the Extruder0 hot end heater to HE0
12. Connect the Extruder1 hot end heater to HE1
13. Connect the bed SSR (DC Control Side) to HE2
14. Connect the Chamber SSR (DC Control Side) to HE3
![Octopus pins and wirings](https://user-images.githubusercontent.com/80109965/224671726-68f2f7fd-ebd2-4f98-8a08-1c051d3678c6.png)

![Bed Heater and Chamber SSR Connections](https://user-images.githubusercontent.com/80109965/226098250-312c27c0-0e9e-404e-a7a7-53ba16267643.png)

