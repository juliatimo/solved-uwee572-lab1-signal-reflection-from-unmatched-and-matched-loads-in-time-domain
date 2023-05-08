Download Link: https://assignmentchef.com/product/solved-uwee572-lab1-signal-reflection-from-unmatched-and-matched-loads-in-time-domain
<br>
This lab is to introduce the basic principle of the signal reflection from unmatched and matched loads in time-domain.  We will also study the method to obtain the value of a small inductance with TDR.

I. Time-domain (TDR) measurements of devices

In Part I, you will use TDS8200 as a TDR (80E04 head) and obtain the reflected voltage from the known and unknown devices.  If a low-loss RF cable is used, the loss compensation may not be needed.  To check the accuracy of your measurement, however, you are asked to measure several known devices.

<strong>Lab Equipment:</strong>

TDS8200 TDR with 80E04 (TDR head)

Figure 1-b: A TDS8200 Digital Sampling Oscilloscope. A Sampling Module

<strong> </strong>

Fig. 1-c Experimental Setup for the Time Domain Analysis of Devices

<strong>Verification load</strong>

SHORT

Matched load (50 ohm)

<strong>Test PCB layout (TL with different Z</strong><strong><sub>o</sub> )</strong>

<strong>Three unknown loads: </strong>Unknown 1, 2, and 3

<ul>

 <li><strong>TDS8200 setup </strong></li>

</ul>

Read the attached file for instruction

Only Ch 1 must be set to TDR (red LED ON).  Under MEASURE. The red LED of Ch 2 must be OFF.

Time scale and number of points: These can be found from Setup-&gt;Hori

<ul>

 <li><strong>Measurement of the verification devices</strong></li>

</ul>

-Attach SHORT to the end of cable and obtain the reflection from it. Save data into PC

-Attach the matched load and obtain the reflection from it.

-Do not attach any devices and measure the reflection (OPEN).

Because the reflection coefficient of a perfect SHORT is -1, the measured waveform can be used for data calibration. How about other two cases?

<ul>

 <li><strong>Unmatched transmission line</strong></li>

</ul>

Connect a test board with the matched impedance (terminated with Z<sub>L</sub>=50) and measure the reflection from it. Save data into PC. Identify the location of the impedance discontinuity and values of the characteristic impedance.  From the measured time delay estimate the dielectric constant and characteristic impedance of each TL section of the board.

Remove the matched load at the end of TL.  This is the OPEN case. Measure data and save the results.  Estimate  and Z<sub>L</sub> of an open circuit from the experimental data.

<ul>

 <li><strong>Unknown loads</strong></li>

</ul>

Measure three unknown loads and save results.  Using the analytical model, estimate the characteristics (capacitive, resistive, inductive, or combination of these?) and values of these loads. See the expected responses and the time-domain responses of complex loads.

<h2>Analysis</h2>

<ul>

 <li>Find the test board TL characteristic impedance and the effective dielectric constantof the center section. Find the reflection coefficient from the experimental data, then obtain the characteristic impedance.  The round time delay can be used to get the effective dielectric constant.  Compare them with the listed values.</li>

 <li>Find <strong>the types and values of unknown loads</strong>. You may use the slope of the [natural log](data) to estimate the time constant.</li>

</ul>

<strong>Estimation of complex load values</strong>

Assume we have a series L and R circuit and we get

where <em>C</em><sub>1</sub> is a constant related to the initial peak voltage of TDR. This is shown as E<sub>i</sub> in the figure. We can assume <em>E</em><sub>total</sub> is also our measured data.  We can find R<sub>L</sub> from either the initial or final condition. If the rise-time is slow, the initial value may be different. In this case, use the final value.  To find <em>L</em>, we set where <em>m</em> is a slope of <em>y=-mt</em> line of the experimental data.  <em>C</em><sub>2</sub> must be positive.  <em>C</em><sub>2 </sub>has a linear section and you can find the slope as <em>m</em>=(A-B)/(t2-t1).  Although E<sub>total</sub> is your measured data, the constant term in <em>C</em><sub>2</sub> is not important.  You can use your experimental data as <em>C</em><sub>2</sub> in the analysis as shown below.

Linear section of C<sub>2</sub> is shown. When we have R and C, we have (1-exp(-<em>m</em>t)) response. In this case you cannot take ln(experimental data) to get a slope.  You need to change the data to get the form exp(-<em>m</em>t)=C<sub>x </sub>equation.

Assume we have a parallel R and C load.

where <em>C</em><sub>1</sub> is a constant related to the initial peak voltage of TDR.  In this expression <em>E</em><sub>total</sub> is your measured data.  Also <em>C</em><sub>3</sub> must be positive to use ln() function.

Another approach is the “trial and error” or “supervised parameter estimation”.  Assume you already know <em>C</em><sub>1</sub> and <em>R</em><sub>L</sub> in the following equation and the only unknown is <em>L</em>.

Set <em>L</em> to be a certain value then calculate E<sub>total</sub>() and compare it with experimental data.  If the tail is too long, <em>L</em> is too large.  If the tail is too short, <em>L</em> is too small.  You may use the “binary search” method to find the optimum value of <em>L</em>.

<h2>PART I is completed.  Close “EE480 TEK11801A VerA” Expected responses  (different TDR is  used for these case)</h2>

(c) Unknown 2                                                        (d) Unknown 3

<strong>Pictures of devices</strong>

Test PCB                                                                                    Unknown device 1

<strong>    </strong><strong>              </strong>

Unknown device 2                                                   Unknown device 3

<h1>II. Small Inductance Measurements Using TDR</h1>

<strong>Objectives:</strong>

An accurate estimate of a small inductance is one of the most important areas in the high speed circuit design.   The delta-I noise, for example, is directly related to the parasitic inductance in both power and ground conductors.  Unlike the measurement of a small capacitor, the small inductance measurement requires an instrument with a very fast risetime and high speed oscilloscope.  In this lab we will study an experimental technique to measure a small inductance in the electronic circuit.  Fig.II-1 shows a measurement setup optimized for characterizing inductors of a few <em>nH</em> (10<sup>-9</sup> H). This arrangement is ideal for measuring the inductance of ground traces or short lengths of conducting wire.

<h2>1. Time-domain measurements</h2>

  Lab Equipment: TDS8200 with 80E04 Channel 1: TDR

Channel 2: TDR LED (red) must be OFF

  Test board <strong>A  (with a short wire) [Do not use test board B]</strong>

Fig.II-1 Test Board A




  Test Cables:  Cable 1: 80E04 channel 1                              Cable 2: 80E04 channel 2

<strong>Note: TDR LED of channel 2 of 80E04 must be OFF.</strong>

<ul>

 <li>characteristics of the input wave form</li>

</ul>

Since we are using raw data, calibration of the TDS8200 is not required.  However, we need to know the rise-time and level of the input voltage.  This can be done by using the THRU (connect cables 1 and 2 directly) measurement.

<ul>

 <li>Connect the cable channel 1 and Channel 2 directly as Fig.II-2.</li>

 <li>Adjust the voltage scale to see the details.</li>

 <li>Using the THRU measurement, obtain the peak voltage and rise time of the input</li>

 <li>Read data into PC and use MATLAB or other software to get the peak voltage and rise-time.</li>

</ul>




Fig. II-2:  Setup for input wave form

<ul>

 <li>The inductance of the DUT</li>

</ul>

-Connect cable 1 to the Test Board port (IN) and cable 2 to the Test  Board port (OUT).




<ul>

 <li>Adjust TDR to see the response.</li>

</ul>




<ul>

 <li>Save the measured data.</li>

</ul>

Fig. II-3: Setup for output wave form

<h2>2. Analysis</h2>

<ul>

 <li>From the measured decay constant, using the relation L = R<sub>s</sub>, compute the inductance of the DUT. If the decay time is too short, skip this part.</li>

 <li>From the measured total area under a response curve, compute the inductance of the DUT. Vinductor</li>

</ul>

<em>dI </em><em>inductor</em>

=<em>L </em>

V<sub>inductor                             </sub><em>dt</em>

∫<em>¥ </em><em>V <sup>inductor</sup></em><sup>(</sup><em>t</em><sup>)</sup><em>dt</em><sup>=</sup><em>L<u>dI </u></em><em>inductor</em>(<em><u>t</u></em>)<em><sub>dt</sub></em>

<sup>0</sup><em>dt</em>

<em> V </em><em>inductor</em>(<em>t</em>)<em>dt</em>=<em>L</em>[<em>I</em>(<em>¥ </em>)−<em>I</em>(0)]               area = L[I() – I(0)]

(<em><u>area</u></em>)           (<em>area</em>)(<em>R<sub>s</sub></em>)

L =          <em>DI       </em> =           <em><sup>DV                                                                                                                                       </sup></em><sub>time</sub>

50:                          toward B

Data Manipulation Using EXCEL and MATLAB

[ EXCEL ]

<ol>

 <li>File  open  “ file name “</li>

</ol>

 Text import wizard-step 1 of 3   next

 Text import wizard-step 2 of 3    comma    next

 Text import wizard-step 3 of 3   finish

<ol start="2">

 <li>“ click “ B ( select row B )   insert    chart</li>

</ol>

 Chart wizard step 1 of 4   area    next

 Chart wizard step 2 of 4    next

 Chart wizard step 3 of 4    next

 Chart wizard step 4 of 4    finish




<ol start="3">

 <li>Integration</li>

</ol>

1) Select the columns not to be used in the integration  delete  save “ file “ 2) Integration Using EXCEL

<ul>

 <li>Row A   time (  t ),   Row B  voltage</li>

 <li>“ Click ” the next  empty cell of the last cell at “ row B “</li>

 <li>“ Click “   *  t</li>

</ul>

Area =   <sub>i </sub>  (  V<sub> i    </sub>*   t )

3) Integration Using MATLAB

load “ file name.Extension “      ( example : file name.extension   lab5.dat )               f1 =  lab5 ( : , 1 ) ;               f2 =  lab5 ( : , 2 ) ;               area = trapz ( f1,f2)

<h1>Appendix I: Laplace transform analysis of a TL terminated with a complex load impedance  (See my lecture note)</h1>

<strong>Expected TDR responses from different complex loads using the unit step function</strong>

<strong>Finite rise-time input (Realistic case and shown in the EE480 note)  </strong>

<strong>Example of the TDR thru data and risetime (Old TEK11801 was used for this)</strong>

SD24-SD22 Thru

<table width="567">

 <tbody>

  <tr>

   <td width="254"><strong>Rise Time For Transmitted Wave (Channel3)</strong></td>

   <td width="24">Channel3</td>

   <td width="11"> </td>

   <td width="254"><strong>Rise Time for Channel 1</strong></td>

   <td width="24">Channel1</td>

  </tr>

 </tbody>

</table>

SD22 Rise-time                                                                                      SD24 Rise-time