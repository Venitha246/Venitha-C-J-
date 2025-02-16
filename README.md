Aim
  Analysis of CS amplifier
  Specifications: 180nm,tsmc,VDD = 1.8v,Power budget = 50uW
  Analysis: DC analysis,Transient analysis,AC analysis
Approch
Task 1
CS amplifier analysis with resistive load
Components Needed
  1.NMOS Transistors: M1(nmos-4).
  2.Resistors: R1(1K ohm).
  3.Power Supply: Vdd(1.8V) for DC supply.
  4. Input Signal Source: Vin(0.9V) signal input.
Circuit Diagram Overview
  1.Transient Setup:
     .M1 (NMOS) as the main amplifying transistor.
     .Gate of M1 is connected to the input node Vin.
     .Source of M1 connected to the ground.
     .Drain of M1 connected to the resistor.
  2. Biasing
    . Vin provides the input signal.
  3. Load Resistors
    . one terminal of resistor is connected to the drain of M1 and the other to Vdd.
DC Analysis
  According to the power budget the required current to operate mosfet in saturation region is 27.7 micro ampears,so to obtain the required current the value of w and L obtained is
     . w=1.7um
     . L=1.8um
Results
     . Vdd=1.8V
     . Vin=0.9V
     . Vout=1.777V
     . Id(M1)=27.737uA
     . Ig(M1)=0A
Transient Analysis
   A sinusoidal input signal of 0.9V peak-to-peak is applied to the gate,and the output voltage is observed at the drain.
Results
   An interveting output curve was obtained when Vin and Vout was plotted against voltage and time with 1ms cycle. Here we can observe a rough 180 degree phase shift between input and output.
AC Analysis
   This AC analysis evaluates the frequency response of a common-source NMOS amplifier.The gain is plotted over a wide frequency range to observe how the circuit amplifies signals at different frequencies and determine its bandwidth limitations.
Results
   The gain remains stable at lower frequencies.
   The amplifier's bandwidth and highlights its frequency-dependent performance.
Task 2 
CS amplifier analysis with PMOS replaced by resistor
     
     
