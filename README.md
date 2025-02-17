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
     * Gain is -26.0dB 
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
# Circuit Diagram 
![WhatsApp Image 2025-02-17 at 11 25 32 PM](https://github.com/user-attachments/assets/18ae9be4-338e-418e-843a-86bae4bee72d)


## DC Analysis
  In this analysis, we determine the biasing conditions of the circuit by calculating the DC operating point (Q-point). The voltages and currents at different nodes of the circuit are analyzed to ensure proper transistor operation. Since the PMOS is replaced by a resistor, the drain voltage (Vd) and drain current (Id) depend on the resistor value and supply voltage. This helps in understanding how the circuit behaves in steady-state conditions before applying any AC signals.
Simulation Setup:-
    In this analysis , a MOSFET with the following dimensions is used:
       CMOSP * Width(W): 1.8um   CMOSN  * Width(W): 1.7um
             * Length(L): 1.8um         * Length(L): 1.8um
       * The drain current(ID) obtained from the LT Spice simulation is: 27.77uA
       * VGS = VG-VS= 0.9-0= 0.9V
       * VDS = VD-VS= 1.8-0= 1.8v
       * VB = 0.1V
From this [Vtn(0.366V)][Vtp(0.39)] VGS >=VTN,Vtp , VDS>=VGS-VTN ,VGS-VTP,then MOSFET is in saturation region.

![WhatsApp Image 2025-02-17 at 11 25 32 PM (1)](https://github.com/user-attachments/assets/c71084b7-9e7a-4fe4-b2e8-8d582304ab4d)

#Conclusion
    The DC analysis of the common-source amplifier with a resistor load helped determine the operating point of the circuit. Replacing the PMOS with a resistor simplified the design but affected the biasing conditions. The drain voltage and current were found to depend on the resistor value and supply voltage. This analysis is crucial as it ensures the transistor operates in the correct region for amplification, providing a foundation for further AC and transient analysis.

## Transient Analysis
   Transient analysis examines the time-domain response of the amplifier to input signals. In this study, a time-varying signal (such as a step, pulse, or sinusoidal input) is applied to observe how the output voltage changes over time. Since the PMOS is replaced by a resistor, the circuit's dynamic response, including signal amplification, delay, and distortion, is analyzed. This helps in understanding the amplifier’s performance for real-time signal processing and determining its stability and response speed.
      * There is a 180 degree phase shift between in input and output 
      * The input voltage(Vin) is applied to the gate(0.9V) 
      * The output voltage(Vout) is measured at the drain = 1.41V.
      
![WhatsApp Image 2025-02-17 at 11 25 32 PM (2)](https://github.com/user-attachments/assets/e2c28f67-2dd3-48a8-bcba-ff2a3d0145a2)
![WhatsApp Image 2025-02-17 at 11 25 32 PM (3)](https://github.com/user-attachments/assets/184f14a7-f4fc-4e5b-ac55-0da442c7bdd0)
# Conclusion
   The transient analysis of the common-source amplifier with a resistor load demonstrated how the circuit responds to time-varying signals. The output waveform showed the amplifier's ability to process dynamic inputs, with variations in gain, delay, and signal distortion. Replacing the PMOS with a resistor affected the overall performance, potentially reducing gain and bandwidth. This analysis is essential for evaluating the amplifier’s real-time behavior and ensuring stable operation for signal amplification applications.

## AC Analysis
 AC analysis examines the frequency response of the common-source amplifier by applying a small-signal AC input and measuring the output. This helps determine key parameters such as voltage gain, bandwidth, and phase shift. With the PMOS replaced by a resistor, the amplifier's gain is affected, as the resistor impacts the output impedance and overall performance. 

* AC amplitude is 50mV
* frequency sweep is 1kHz
* DC offset is 0.9V

![WhatsApp Image 2025-02-17 at 11 25 32 PM (4)](https://github.com/user-attachments/assets/2f0671a6-b2da-4dfc-acb3-aa3d1c14583b)
  * Gain is -26.0dB 
  * Av= Vout / Vin = 1.41-1.14/950m-850m = 2.7
# Conclusion
   The AC analysis of the common-source amplifier with a resistor load provided insights into its frequency response. The voltage gain was influenced by the resistor value, affecting the overall amplification. The bandwidth and cutoff frequencies were identified, showing the range over which the amplifier operates effectively. 

## INFERENCE
Through this analysis, I understood how the common-source amplifier behaves in different conditions. DC analysis helped in finding the operating point and ensuring proper biasing. AC analysis showed how the amplifier responds to different frequencies, with gain and bandwidth depending on the resistor load. Transient analysis provided insights into how the amplifier processes time-varying signals.
Replacing the PMOS with a resistor made the circuit simpler but reduced the gain and affected the frequency response. This showed me the trade-offs involved in amplifier design and how different components impact performance.
  
           


  




  




    
