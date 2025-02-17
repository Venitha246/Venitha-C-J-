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
![WhatsApp Image 2025-02-17 at 9 31 00 PM](https://github.com/user-attachments/assets/27e1e56f-6a76-4c00-a28a-a9510946481a)
![WhatsApp Image 2025-02-17 at 9 31 00 PM (1)](https://github.com/user-attachments/assets/e5c1d8da-4af8-47a8-87ab-a3cf33f20b71)
# Conclusion :-
      The transient analysis shows that the common-source amplifier performs as expected.The output voltage tracks the input voltage with a reasonable rise time .This confirms the amplifiers stable behaviour in the time domain.

## AC Analysis
     This Analysis is to evaluate the frequency response ,gain,and impedance characteristics over a range of frequencies.
     * AC amplitude is 50mV
     * frequency sweep is 1kHz
     * DC offset is 0.9V
![WhatsApp Image 2025-02-17 at 9 46 12 PM](https://github.com/user-attachments/assets/df47ed7f-f8a4-48ae-b97d-a9e932b3bd55)   
     * Gain is 26.3dB 
     * Av= Vout / Vin = 1.777-1.767/950m-850m = 0.1
# Conclusion:-
     The amplifier provides stable gain within the mid-band. The bandwidth and gain values are consistent with expectations for a common-source amplifier.

## INFERENCE
    The common-source amplifier was analyzed using DC, AC, and transient analysis in LTspice. DC analysis set the biasing, AC analysis showed a  gain, and transient analysis revealed signal behavior. The experiment confirms efficient amplification.


## Task 2 
# CS amplifier analysis with PMOS replaced by resistor
# INTRODUCTION
     The PMOS typically serves as the active load ,providing higher output impendance and improving voltage gain.This modification helps in understanding the impact of load resistance on the amplifiers behaviour and performance ,serving as a foundation for further optimization .
    1. DC ANALYSIS: Finds the operating point of the MOSFET by checking voltage and currents.
    2. AC ANALYSIS: Measures the gain and frequency response to see how well the amplifier works at different frequencies.
    3. TRANSIENT ANALYSIS: Observes how the amplifier responds to a time-varying signal.
# Components Required
    * PMOS4 AND NMOS4 Transistor: CMOSP(M1),CMOSN(M2)
    * Power Supply: V1(1.8V) for DC supply
    * Input Signal Source: V3(0.9V) Signal input
    * Bias voltage (Vb):
        to keep both transistors in saturation
           VTH<VIN<VOUT+VTH
           VIN-VTHN<=VOUT<=VDD-Vb-|VTHP|
           0.9-0.366<=VOUT<=1.8-Vb-0.39
           0.54<=Vb<=-1.41+1.8
           0.54<=Vb<=0.39
           
           


  




  




    
