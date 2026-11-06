--- page 1 ---
Development of Triaxial MEMS Digital

Accelerometer on Structural Health Monitoring

System for Midrise Structures

Jamie Eduardo C. Rosal; Meo Vincent C. Caya

School of Electrical, Electronics, and Computer Engineering, Mapua University, Manila, Philippines

jamiewertalmighty@gmail.com; mvccaya30@gmail.com

Abstract—Damage detection and characterization using

nondestructive methods in structural and civil engineering

progresses significantly in utilizing structural health monitoring

techniques but, implementation issues still exist such as poorly

calibrated sensors prompting low data accuracy. This study

aims to measure the characteristics of the ADXL 345

accelerometer in the laboratory and during working conditions.

Calibration technique used was a subwoofer method and yielded

96.3481% accuracy and measured the vibration on a particular

building. Consequently, the system is capable of measuring

frequency response and acceleration measurement that is

important in structural health monitoring.

Keywords— Structural health; acceleration data; vibration

monitoring

I. INTRODUCTION

Structures are built to protect us from natural phenomena.

It is important that our buildings are healthy and monitored

from severe structure loadings such as earthquakes [1],

typhoons [2, 3], and active daily loading and overloading with

heavy contents  which cause substantial economic loss.

Moreover, this can bear continuing damage when structural

integrity deteriorates gradually overtime [4] [13]. Structural

health monitoring (SHM), which can tone down high repair

cost by monitoring and discovering these detrimental

circumstances as they take place and has develop into a

fundamental instrument to enhance engineers improve safety

and maintain significant infrastructures. The need to develop

this technology is essential in keeping our structures safe and

generated information to improve future structural designs.

Different methods, calibration and measurement techniques

were developed and used to collect, calibrate and measure

vibrations on structural health monitoring. Experimental

design was employed to combine subwoofer method for

frequency response and inclination sensing method of

calibration to accelerometers, resulted to a huge accuracy

levels another calibration technique was used to a number of

temperature sensors called Two-point calibration method,

resulted to not more than 10% percent error and considered

to be with high data integrity, resulted from checking and

experimenting on structural acceleration, vibration,

temperature drifts, and surroundings temperature information

from a concrete bridge experiment podium. The method of

experimentation on sensing distinctiveness of the sensors

resulted on a winning improvement [6]. The experimental

method was used to certify the information output of

accelerometers. A shaking stimulator was attach on a

centrifuge was created that provided synchronized harmonic

constant linear accelerations. The calibration method

involved was used to assess the shaking refinement

inaccuracy of the accelerometer [7]. Another technique was

used to investigate the causes of three-axis digital

accelerometer MPU6050 errors using the Maximum

likelihood estimation (MLE) method. The method involved

the rotating the accelerometer which was setup on one

hundred hertz (100hz) data rate on the X,Y and Z  axis, after

the process, computation of acceleration data averages for

each axis. With recurring procedure the averages were used

as input to the MLE algorithm. MLE-based algorithm

obtained a high precision estimation in acceleration data [8].

a different  data  gathering method which decrease  the

variance of parameter estimation  of  a micro electro-

mechanical accelerometer sensors using optimum

experimental design via a auto-calibration model with the aim

of rotatable and gravity optimal[9]. Another method of

calibration was experimented to determine linear velocity and

adjust the untreated data of an accelerometer by means of an

encoder utilizing fuzzy inference systems technique. [10].

As a result, Modern methods and technologies that deals

with accelerometer sensors which can promote improvement

of the qualifications of sensor sensing in acceleration

monitoring and frequency response of structures.

The goal and idea of this study is to develop a structural

health monitoring system that collects vibration data from

structures to help engineers improve safety and structure

maintainability. Particularly, it aims to calibrate the

accelerometer to ensure profound data integrity in structural

health monitoring using inclination sensing and subwoofer

calibration methods, and test the develop system on a midrise

structure.

--- page 2 ---
II.  MATERIALS AND METHODS

A. System Hardware

The SHM system was made-up using industrial grade

plastic container housing the onboard computer and the

accelerometer sensor. It consists of a Raspberry Pi 3 Model

B+ and the ADXL 345 accelerometer sensor connected via

I2C port of the Raspberry Pi 3 Model B+ as shown in Figure

1.

Fig. 1. System Hardware: (a) ADXL 345 accelerometer, (b) Raspberry Pi 3

Model B+.

B. Calibration of ADXL 345 sensor

To calibrate the ADXL 345 accelerometer sensor to

ensure profound data integrity, a two phase procedure is

implemented first is testing and adjusting for preference on

tilting, second is the vibration excitation experiment using the

subwoofer method[11].Adjustment of the acceleration

reading on the accelerometer is made by recording

unprocessed data on the three axes x, y and z such as highest

and lowest acceleration readings to compute the increase and

determine the difference on acceleration values.  The

rectangular casing of system hardware was used as the

reference frame as shown in Figure 2. The casing houses the

accelerometer in a straight leveled position in order for

gravity to be directly sensed for one g force (1g) in the z-axis.

A txt file which is stored in the computer system memory

hold the acceleration data of the highest and lowest values of

the three (3)  axes and the calculated difference and increases

of the acceleration readings that is essential for the next phase

of testing and calibration. Equation 1 is the accelerometer

output, simultaneously with the difference and sensitivity errors:  [Equation 1]

The difference error on readings in g AOUT is the offset,

while the increase on acceleration readings is the Gain having

an expected value of one g(1g), the true acceleration reading

and the preferred value AACTUAL is the real gravity force.

taking into consideration the calculated measurements of the

three axis and two end points of each which is positioned in

the positive one g(1g) and negative one g(-1g) of gravity is

shown in  Equation 1 and Equation 2.

[Equation 2] [Equation 3]

These points are used to calculate the difference and increase of the accelerometers reading, as mentioned in the maximum- and minimum-acceleration end-point equations

[Equation 4] [Equation 5]

Therefore, the difference from the real

accelerometer readings is calculated by the increase readings

for the real actual calibrated reading.

[Equation 6]

The actual real accelerometer readings was the bases for

computation  written  in to a raspberry pi script   formatted

for timestamp,  x, y and z axes in a txt file and was  used for

the next phase of adjustment.  The experimental method of

testing the vibration readings and functionality of the

accelerometer sensor by means of certifying the frequency

response difference is the subwoofer calibration technique to

check if the accelerometer readings are identical to the

frequency generated value of the function generator.  Figure

3. Calibration block diagram of the Subwoofer method.

Fig. 2. Accelerometer point of reference for x-axis, y-axis and z-axis for

positive and negative using the rectangular casing as reference frame.

--- page 3 ---
Fig. 3. Subwoofer-setup block diagram

To test out if the accelerometer readings and the

frequency generated value of the function generator are

identical values a subwoofer speaker whose input is the

frequency generated value of the function generator [11].The

experimental procedure of the subwoofer method was on

configuring the function generator to output one

hertz(1hz),two(2hz),three hertz(3hz) and  four(4hertz) with

regular voltage and sinusoidal  wave as input to the

loudspeaker which stimulate vibration on the plate of the

speaker, the accelerometer is setup to ± 2g  is  enclosed in a

rectangular casing connected to raspberry pi computer

running a python script which outputs a txt file that hold

untreated vibration readings  and  adjusted acceleration

measurements with the up and down movement of the

acceleration which is the z-axis measurements is prioritize .

The raspberry pi was setup to run and read ten (10)

acceleration data per second. To validate the frequency input

signal of the function generator an oscilloscope was used      as

shown in figure 2 was mounted on the top of the speaker

panel of the subwoofer.

Fig. 4. Subwoofer-setup calibration flow chart

Fig. 5. Actual subwoofer-setup calibration.

To generate the frequency spectrum of the

acceleration readings and to establish the frequency values a

fast Fourier transform algorithm was used implemented in

using Numerical Python to determine the Discrete Fourier

Transform of the acceleration data in a time series [12].

The accelerometer frequency readings A f after a

minute will be compared to the input frequency from the

function generator S f. the frequency readings from the

accelerometer and the function generator has  more than 10%

Percent Error; the accelerometer will be recalibrated until the

value coincides. The Percent Error is defined in Equation 8.

[Equation 8]

C. Deployment and Testing

The deployment place is a-three year old four storey

midrise building named Coidre Building in Cor Jesu College

a school building in Davao del Sur, Philippines which is

shown in Figure 6. Upon consultation with an expert civil

engineer on what optimal location is the SHM system would

be mounted in the 3 rd floor ceiling beam as suggested which

directly supports two classrooms promoting z-axis vibrations

[14]. The SHM system was configured to retrieve for seven

days [15]. Figure 7 shows the SHM system mounted on the

beam.

--- page 4 ---
Fig. 6. Coidre building in Cor Jesu College Digos City, Philippines

Fig. 7. SHM system mounted on the 3rd floor beam of Coidre building

III. RESULTS AND DISCUSSIONS

Essential acceleration data were collected processed and

analyzed using Fast Fourier Transform in Numerical

Python.

Calibration of ADXL 345 sensor

The testing results of the vibration and frequency response of

the accelerometer as shown in Table I was conducted with

four testing cases were verified and compared and yielded a

mean percent error of 3.6519%, and standard deviation of

0.0465% respectively. The data also show a T-statistic of 2.1

which confirms that the frequency response of the

accelerometer and of the speaker frequency have no

significant difference on 0.10 significance.

Result of SHM system deployment on test structure

Table II, shows the results of the one week testing of SHM

system on the Coidre building which has acceleration value

of 0.9824 (g)  though the deployment period and mean daily

maximum and minimum acceleration values of 1.0053(g),

0.958687083(g),  respectively.

The time series representation of acceleration as shown in

figure 8 illustrates the movement of the beam being

monitored beam movements increases in when subjected to

active loads and decreases on dead loads.

Fig. 8. Time Series representation of acceleration of the 3rd floor beam of

Coidre building

IV. CONCLUSION AND FUTURE WORKS

In this study, a structural health monitoring system

is developed and applied the inclination sensing and

subwoofer-setup calibration technique and successfully

calibrated the accelerometer used on the SHM system which

resulted on a percent error of 3.6519%. The SHM system

which was deployed on the test structure gathered significant

data which suggest that the difference between mean

maximum, minimum and total daily acceleration confirms

that SHM system detected the vibrations on the test building.

Implementation on multiple beams on midrise structure and

comparison of data is recommended.

Table I. Accuracy of the functionality of accelerometer

Test No.

Accelerometer

Frequency (Hz)-

Af

Speaker

Frequency

(Hz)-Sf

Difference-

Df

Percentage Error

(%)

1 0.91069 1 0.08931 9.806849751

2 1.91776 2 0.08224 4.288336392

3 3.01034 3 -0.01034 -0.343482796

4 3.96605 4 0.03395 0.856015431

Table II. Coidre building accelaration readings

Day no.

Max

acceleration

value reading

of X-axis (g)

Min acceleration

value reading of

X-axis (g)

Mean of daily

acceleration readings

(g)

1 1.0238 0.95782994 0.9828

2 1.0058 0.95982994 0.9828

3 1.0098 0.94582994 0.9819

4 0.9998 0.96182994 0.9828

5 0.9938 0.97382994 0.9834

6 1.0018 0.95382994 0.9822

7 1.0018 0.95782994 0.9812

--- page 5 ---
REFERENCES

[1] M. Roghaei and A. Zabihollah, “An Efficient and Reliable Structural

Health Monitoring Systemfor Buildings after Earthquake”, APCBEE

Procedia 9, pages 309 – 316,2014

[2] Ruicong Han, Xuefeng Zhao,Yan Yu, Quanhua Guan,Deli

Peng,Mingchu Li, and Jinping Ou1, "Emergency Communication and

Quick Seismic Damage Investigation Based on Smartphone"

,Advances in Materials Science and Engineering Volume 2016, Article

ID 7456182,2016

[3] Sholihin A a* , Mukahara , and M. Sukimanb,”Investigation on Wall

Crack Damage and Its Proposed Repair Method, Procedia

Engineering” Volume 54, Pages 165-175,2013.

[4] Qingxia Zhang and Lukasz Jankowski, ”Damage identification using

structural modes based on substructure virtual distortion method”,

Advances in Structural Engineering  1-15, 2017.

[5]  Ichitsubo,M.Horiguchi, I.Nagamachi , “ A study on the evaluation of

structure damages for the visual inspection”, Proceedings of the 2005

International Conference on Active Media Technolog 2017, Vol. 20(2)

257–271,2017

[6] R.S. Concepcion II , F.R.G. Cruz , F. A. A. Uy, J.M.E. Baltazar , J. N.

Carpio, K. G. Tolentino, “Triaxial MEMS Digital Accelerometer and

Temperature Sensor Calibration Techniques for Structural Health

Monitoring of Reinforced Concrete Bridge Laboratory Test Platform”,

IEEE 2017.

[7] Guan, X. Meng, X. Dong, “Calibration of accelerometer with

multicomponent inputs”, IEEE Instrumentation and Measurement

Pages 16 – 19,2014

[8]  X. Lu, Z. Liu, J. He, “Maximum likelihood approach for low-cost mems

triaxial accelerometer calibration”, IEEE 8 th International Conference

on

Intelligent Human-Machine Systems and Cybernetics, 179-182,2016

[9] L. Ye, S. Su, “Optimum experimental design applied to

memsaccelerometer calibration for 9-parameter auto-calibration

model”, IEEE Engineering in Medicine and Biology Society

Conference, 2015

[10] S. Woo, Ja. Kim, Ju. Kim, S. Kim, “Calibration of accelerometer using

fuzzy inference system”, IEEE Control, Automation and

SystemsConference, 2093-7121,2001

[11] D. Litwhiler, “A custom vibration test fixture using a subwoofer”, Penn

State University, Paper 068 ENT 205, 2011.

[12] G. Strang, “Wavelets”, American Scientist 82, 1994.

[13] O. Weeger,U. Wever and B. Simeon, “Nonlinear frequency response

analysis of structural vibrations”, Comput Mech (2014) 54:1477–

1495,2014

[14] John C Moore et al  “Regional Timber Bridge Girder Reliability:

Structural Health Monitoring and Reliability Strategies”, Advances in

Structural Engineering Vol. 15 No. 5 2012.

[15] S. Cho, C-B. Yun, J. Lynch, A. Zimmerman, B. Spencer, T.

Nagayama,

“Smart wireless sensor technology for structural health monitoring of

civil structure,” Steel Structures (8), 267-275,2008