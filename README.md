Download Link: https://assignmentchef.com/product/solved-ece4830-lab4
<br>
<h1>3.1 Rational Z-transforms</h1>

As noted in your textbook, the common Z-transform pairs can be written as a ratio of two polynomials in <em>z</em><sup>-1</sup> or <em>z</em>. That is <em>H</em>(<em>z</em>) <em>ND</em>((<em>zz</em>)) <em>b</em>0 <em>b</em>1<em>z</em><sup></sup>11L<em>ba</em><em>MNzz</em><em>MN</em>

<em>a</em>0 <em>a</em>1<em>z </em>L

If we know that a system can be described by <em>H</em>(<em>z</em>), its output to a known input <em>X</em>(<em>z</em>) can be computed by multiplying <em>H</em>(<em>z</em>)<em> X</em>(<em>z</em>). On the other hand, if we know the input <em>X</em>(<em>z</em>) and the output <em>Y</em>(<em>z</em>), the system can be identified. The time domain solution can be easily obtained by using partial-fraction expansions.

<strong>Problem 1. </strong>

Consider the system:

<h1>z<sup>2 </sup>z H(z) z<sub>2 </sub>3z<sub></sub>2</h1>

How many poles and zeros do you have?




Poles _______




Zeros _______




Use the command <em>roots</em> in Matlab to determine the numerical values of these poles and zeros.  Use roots([1 –1 0]) for the zeros and roots([1 3 2]) for the poles.




Poles =




Zeros =




Describing the same system in terms of increasing order of <em>z</em><sup>-1</sup>, we have 1<em>z</em>1

<em>H</em>(<em>z</em>)1 1 2<em>z</em>2 3<em>z </em>

Use roots([1 –1]) for the zeros and roots([1 3 2]) for the poles. Do you have the same answer?







Poles =




Zeros =










Compute <em>h</em>(<em>n</em>) using the poles and zeros found with Matlab.







<em>h</em>(<em>n</em>) =

<strong>Problem 2 </strong>

Use the <em>filter</em> command in Matlab to generate and plot the impulse response <em>h</em>[<em>n</em>] of the following second order difference equation. Plot <em>h</em>[<em>n</em>] in the range of –10  n  100.

<em>y</em>[<em>n</em>] – 1.8cos(/16)<em>y</em>[<em>n</em>-1] + 0.81<em>y</em>[<em>n</em>-2] = <em>x</em>[<em>n</em>] + 0.5<em>x</em>[<em>n</em>-1]

Determine the impulse response using the inverse Z-transform and confirm your results.

<h1>3.2 Frequency response of difference equations</h1>

The frequency response of a system <em>h</em>(<em>n</em>) can be obtained by evaluating the z-transform of the system on the unit circle. That is, if a system is described by <strong> </strong>

<em>K</em>

(<em>z </em> <em>z<sub>k </sub></em>)

<em>H</em>(<em>z</em>)  <em>A </em><em><sup>k</sup><sub>M</sub></em><sup>1     </sup>,

(<em>z </em> <em>p<sub>m </sub></em>)

<em>m</em>1




the contribution of each pole and each zero to the magnitude in the frequency domain depends on the length of the vector from the pole or zero to the point <em>e <sup>jw </sup></em>. Thus, taking the magnitude and evaluating at <em>e <sup>jw </sup></em>yields:

<em>K                                       K</em>

| <em>e <sup>jw </sup></em> <em>z<sub>k </sub></em>| v<em><sub>k</sub></em>

| <em>H</em>(<em>e </em><em>jw</em>)| <em>A </em><em>kM</em>1

| <em>e <sup>jw </sup></em> <em>p<sub>m </sub></em>| u<em><sub>m</sub></em>

<em>m</em>1                                   <em>m</em>1

as shown in the next figure.




The phase is given by

<em>K                                 M</em>

<em>H</em>(<em>e <sup>jw</sup></em>) <em>A</em>(<em>e <sup>jw </sup></em> <em>z<sub>k </sub></em>)(<em>e <sup>jw </sup></em> <em>p<sub>k </sub></em>)

<em>k</em>1                              <em>m</em>1

<strong> </strong>

<strong>Problem 3. </strong>




Plot the poles and zeros of the system in Problem 2.










Using the command <em>freqz</em>, plot the magnitude and phase of the frequency response of this system. If the system is to be defined as a filter, what kind of filter it is?







Filter is ____________________________







Do the same for the following filters:




<ul>

 <li><em>y</em>[<em>n</em>] + 0.13<em>y</em>[<em>n</em>-1] + 0.52<em>y</em>[<em>n</em>-2] + 0.3<em>y</em>[<em>n</em>-3] = 0.16<em>x</em>[<em>n</em>] – 0.48<em>x</em>[<em>n</em>-1] + 0.48<em>x</em>[<em>n</em>-2] –</li>

</ul>

0.16<em>x</em>[<em>n</em>-3]







<em>H</em>(<em>z</em>) =







____________________________________________










Filter is ____________________________




<ul>

 <li><em>y</em>[<em>n</em>] – 0.268<em>y</em>[<em>n</em>-2] = 0.634<em>x</em>[<em>n</em>] – 0.634<em>x</em>[<em>n</em>-2]</li>

</ul>







<em>H</em>(<em>z</em>) =







____________________________________________










Filter is ____________________________




<ul>

 <li><em>y</em>[<em>n</em>] + 0.268<em>y</em>[<em>n</em>-2] = 0.634<em>x</em>[<em>n</em>] + 0.634<em>x</em>[<em>n</em>-2]</li>

</ul>







<em>H</em>(<em>z</em>) =







____________________________________________










Filter is ____________________________




<ul>

 <li>10<em>y</em>[<em>n</em>] – 5<em>y</em>[<em>n</em>-1] + 2<em>y</em>[<em>n</em>-2] = <em>x</em>[<em>n</em>] – 5<em>x</em>[<em>n</em>-1] + 10<em>x</em>[<em>n</em>-2]</li>

</ul>







<em>H</em>(<em>z</em>) =







____________________________________________










Filter is ____________________________



















Without taking into consideration the cut-off frequencies, draw the poles and zeros of the simplest low-pass and high-pass filters you can think of. That is, use a minimum number of poles and zeros. Explain your results.



















You will be given an acoustic signal in the file BoatWhale.mat. Note that the signal is already in Matlab format. The samples correspond to a recording using a hydrophone of a whale sound but it also records the sound of the boat (Fs = 22050Hz). Design a filter that can attenuate the sound of the boat. Please include the pole-zero diagram and your methodology.

Matlab instructions that can help you:

To listen to the audio use <em>sound</em>

To obtain a polynomial from roots use the command <em>poly </em>The command <em>tf</em> can give you the pole-zero plot.

Hint, the sound of the boat has a good number of harmonics.