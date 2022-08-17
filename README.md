# MICRO-LAB-4
 # OBJECTIVES
The main objective of this lab is for you to develop a small water level controlling system of a water tank using the knowledge of interrupts and other programming techniques of PIC16f877a from all the labs we did throughout the course.<br>

# INTRODUCTION
The purpose of the project is to create a system that automatically controls the water level. The implementation of the proposed system is based on PIC microcontroller and 3 infra-red sensors, which is used to measure the water level within a tank and based on this measurement, the two DC motors are turned ON or OFF automatically. The experimental results show that the proposed system is succeed in measuring the water level and turning the water pump ON or OFF according to the water level<br>

Electronic circuits known as PIC microcontrollers can be configured to perform a wide variety of activities. They can be programmed to act as timers, manage a production line, and do a lot more things. A PIC microcontroller can be programmed using a number of different software. There are people who still use Assembly language to program PIC Microcontrollers.<br>

An electrical device that monitors and detects infrared radiation in its environment is called an infrared (IR) sensor. Infrared sensors come in active and passive varieties. Infrared radiation is both produced and detected by active infrared sensors. A light emitting diode (LED) and a receiver are the two components of an active IR sensor. The receiver detects the infrared light from the LED that reflects off an object as it gets close to the sensor.<br>

DC motors are used in this system. A sort of electric machine that transforms electrical energy into mechanical energy is a direct current (DC) motor. Direct current (DC) motors take electrical power and turn it into mechanical rotation. With the help of magnetic fields produced by electrical currents, DC motors rotate a rotor placed within the output shaft. The electrical input and the motor's design both affect the output torque and speed.<br>

A printed circuit board, or PCB, is used to mechanically support and electrically connect electronic components using conductive pathways, tracks or signal traces etched from copper sheets laminated onto a non-conductive substrate. All the components here are connected through the pcb board.<br>

# APPARATUS
•	PCB board<br>

<img align="center" src="https://user-images.githubusercontent.com/109506465/185037522-f8b3e884-5929-4370-bbb1-eb9358d142c9.jpg" width= 300>

•	PIC16F877A<br>

<img src="https://user-images.githubusercontent.com/109506465/185038846-1c6a6abd-6805-4bcc-a1d2-6640806067b7.jpg" width= 350>

•	DC motors<br>

<img src="https://user-images.githubusercontent.com/109506465/185038498-de87f755-51a9-4a87-8663-4b47a848ec76.jpg" width= 250>

•	IR sensors<br>

<img src="https://user-images.githubusercontent.com/109506465/185039263-8b408a2f-6657-4e28-8f6a-56dab7e473c5.png" width= 250>

•	Wires<br>

<img src="https://user-images.githubusercontent.com/109506465/185040098-4cefb9ee-ee9e-4ec9-a173-c030aff457db.jpg" width= 300>

•	Motor module<br>

<img src="https://user-images.githubusercontent.com/109506465/185040292-5609fc82-6010-4c07-9ab4-875669bb8978.jpg" width= 300>

•	Capacitors<br>

<img src="https://user-images.githubusercontent.com/109506465/185040456-2dcb759c-49c1-4589-9b72-989c1854ba30.jpg" width= 300>

•	Crystal oscillator<br>

<img src="https://user-images.githubusercontent.com/109506465/185040537-6784263a-2bd3-474b-8122-099102915751.jpg" width= 300>

•	Pic adaptor<br>

<img src="https://user-images.githubusercontent.com/109506465/185040713-72d7c49c-a4d5-4215-8adf-1d13939de1c0.jpg" width= 300>

•	Soldering iron<br>

<img src="https://user-images.githubusercontent.com/109506465/185040999-1a100701-3bc6-42af-8c10-b6414bfb8916.jpg" width= 300> <br>

# PROCEDURE

1.	First the pcb design was created using the proteus software.<br>

2.	Then the pcb board was made by using that design. To make it a cu board and ferric chloride was used.<br>

3.	And then the components used are soldered to the pcb board as in figure 14 <br>

4.	Then the code that use to program the pic microcontroller was written using the MP labs software and uploaded it into the pic microcontroller using pickit 3.<br>

5.	Then it was connected to the pcb board using the pic adaptor.<br>

6.	After that three sensors and the motor module was connected to the pic16F877A.<br>

7.	Then the motors were connected to the motor module.<br>


# Operation Table

<img src="https://user-images.githubusercontent.com/109506465/185041891-6fb06f14-1dae-4aaa-a616-506e8d97cb01.png" width= 1200>


# DISCUSSION
There are two DC motors in this system, one of which pumps water into the tank and the other of which suctions water out of the tank. The water level in the tank is also monitored by three IR sensors. When the IR sensors detect and object it gives a logic low output. According to the above table 1, in the first instance when switch one is on and switch two and three are off the motor one pump the water into the tank and motor two is off. In the second instance when switch one and two are on and switch three is off, motor one pump the water into the tank   and the motor two is off. In the third one when all three switches are on, the motor two suck the water out from the water tank for 500 milliseconds and then it turns off and motor one is off in that instance. Depending on the water level the micro controller produces a logic high or low to turn the switches on and off. And the IR sensors we used in here has a low level trigger output.<br>

In this system switch one is connected to the pin 2 of the PORT B in the pic16F877A microcontroller. And switch 2 is connected to the pin 1 of PORT B and switch 3 to pin 0 of PORT B. then the motor 1  motor 2 are connected to the pin o and pin 1 in PORT C respectively. <br>

<img src="https://user-images.githubusercontent.com/109506465/185042566-fdff4cd1-1b7b-431c-bcb8-3d16feca7640.png" width= 500 >

# THE DESIGNED SYSTEM

<img src="https://user-images.githubusercontent.com/109506465/185121591-14dfd617-ce7d-43f7-b0e4-f159534b197f.jpg" width= 500>

<img src="https://user-images.githubusercontent.com/109506465/185126250-f573a4f1-a9a3-4f11-be6d-2290c5fc1d25.jpg" width= 200>

<img src="https://user-images.githubusercontent.com/109506465/185127735-8fa74623-04a1-42bd-af1f-7b04cda38476.jpg" width= 200>

<img src="https://user-images.githubusercontent.com/109506465/185128484-b943745d-5ee0-4a2d-b4e1-fb8283a6c6c2.jpg" width= 200>

# CODE USED

#pragma config FOSC = HS        // Oscillator Selection bits (HS oscillator)<br>
#pragma config WDTE = OFF       // Watchdog Timer Enable bit (WDT disabled)<br>
#pragma config PWRTE = OFF      // Power-up Timer Enable bit (PWRT disabled)<br>
#pragma config BOREN = OFF      // Brown-out Reset Enable bit (BOR disabled)<br>
#pragma config LVP = OFF        // Low-Voltage (Single-Supply) In-Circuit Serial Programming Enable bit (RB3 is digital I/O, HV on MCLR must be used for programming)<br>
#pragma config CPD = OFF        // Data EEPROM Memory Code Protection bit (Data EEPROM code protection off)<br>
#pragma config WRT = OFF        // Flash Program Memory Write Enable bits (Write protection off; all program memory may be written to by EECON control)<br>
#pragma config CP = OFF         // Flash Program Memory Code Protection bit (Code protection off)<br>



#include <xc.h><br>
#include<htc.h> <br>

#define _XTAL_FREQ 20000000<br>


void __interrupt() isr(void){<br>
    if(RB1 ==1 && RB2 ==1){<br>
        RC0 =0;<br>
        RC1 =1;<br>
        __delay_ms(500);<br>
        RC1 =0;<br>
    }<br>
    INTF =0;<br>
}<br>

void main (void){<br>
    INTF =0;<br>
    INTE =1;<br>
    GIE =1;<br>
    INTEDG =1;<br>
    
    TRISB0 =1;  //SWITCH 3
    TRISB1 =1;  //SWITCH 2
    TRISB2 =1;  //SWITCH 1
    TRISC0 =0;  //MOTOR 1
    TRISC1 =0;  //MOTOR 2
    
    while(1){
        if(RB2 ==1 && RB1 ==0 && RB0 ==0){
            RC0 =1;
        RC1 =0;
        }
         if(RB2 ==1 && RB1 ==1 && RB0 ==0){
            RC0 =1;
        RC1 =0;
        }
         if(RB2 ==0 && RB1 ==0 && RB0 ==0){
            RC0 =0;
        RC1 =0;
        }
    }
    return();
}

# REFERENCES

•	George, L. and George, L., 2022. Water Level Indicator Controller Using PIC Microcontroller. [online] electroSome. Available at: <https://electrosome.com/water-level-indicator-controller-pic/> [Accessed 18 July 2022]. <br>

•	2022. [online] Available at: <https://www.researchgate.net/publication/335210568_PIC_Microcontroller_Based_Water_level_Monitoring_and_Controlling_System_using_Sharp_Infra-red_range_sensor> [Accessed 18 July 2022].<br>

•	2022. [online] Available at: <https://livetechindia.com/water-level-indicator-using-micro-controller-pic16f877a/> [Accessed 18 July 2022].<br>

•	2022. [online] Available at: <https://www.fierceelectronics.com/sensors/what-ir-sensor> [Accessed 18 July 2022].<br>











