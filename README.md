# Venitha C J
# LINEAR INTEGRATED CIRCUITS
# Experiment 1
## AIM
    To obtain the DC analysis ,AC analysis ,Transient analysis of a Common Source(CS)amplifier and also obtain gain and other parameters using LT spice.
## INTRODUCTION 
    A Common Source amplifier is a basic MOSFET-based circuit used circuit to amplify signals. In this circuit the input is applied to the gate , the source is connected to ground and the output is taken from the drain.
    1. DC ANALYSIS: Finds the operating point of the MOSFET by checking voltage and currents.
    2. AC ANALYSIS: Measures the gain and frequency response to see how well the amplifier works at different frequencies.
    3. TRANSIENT ANALYSIS: Observes how the amplifier responds to a time-varying signal.
# Components Required
     NMOS4 Transistor: M1(CMOSN)
     Resistor: R1(1K ohm)
     Power Supply: V1(1.8V) for DC supply
     Input Signal Source: V2(0.9V) Signal input
# Circuit Diagram
![WhatsApp Image 2025-02-17 at 8 51 09 PM](https://github.com/user-attachments/assets/9467633c-ef24-4429-82ab-8cf156cc963e)

## DC Analysis
      This analysis helps in finding the biasing conditions ,ensuring that the transistors operates in the saturation region for proper amplification 
Simulation Setup:-
    In this analysis , a MOSFET with the following dimensions is used:
       * Width(W): 1.7um
       * Length(L): 1.8um
       * The drain current(ID) obtained from the LT Spice simulation is: 27.77uA
       * VGS = VG-VS= 0.9-0= 0.9V
       * VDS = VD-VS= 1.8-0= 1.8v
From this [Vtn(0.366V)] VGS >=VTN , VDS>=VGS-VTN ,then MOSFET is in saturation region.
# Conclusion:-
     The DC analysis results ensure that the MOSFET is correctly biased,providing the foundation for further AC and Transient Analysis to study the amplifiers gain and frequency response.
![WhatsApp Image 2025-02-17 at 8 51 09 PM](https://github.com/user-attachments/assets/bff711a4-1d3b-4a29-8414-af5f54c8f936)
![WhatsApp Image 2025-02-17 at 9 17 42 PM](https://github.com/user-attachments/assets/3f339970-27b3-46d1-8d4e-c48c142685eb)

## Transient Analysis
      This analysis was conducted to observe how the common-source amplifier responds to a time-varying input signal.
      * There is a 180 degree phase shift between in input and output 
      * The input voltage(Vin) is applied to the gate(0.9V) 
      * The output voltage(Vout) is measured at the drain = 1.777V.
  




  




    
