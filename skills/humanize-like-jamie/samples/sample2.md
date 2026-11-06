--- page 1 ---
Ripeness Classification of Cacao Using Cepstral-

Based Statistical Features and Support Vector

Machine

Juvy Amor M. Galindo1, Jamie Eduardo C. Rosal 2, Jocelyn Flores Villaverde 3

1, 2 College of Engineering and Technology

Cor Jesu College, Inc.

Digos City, Philippines

Email: juvyamorgalindo@gmail.com 1, Jamiewertalmighty@gmail.com 2

3 School of Electrical, Electronics and Computer Engineering

Mapua University

Manila, Philippines

Email: jfvillaverde@mapua.edu.ph 3

Abstract—High quality fine cocoa beans come from farms

on which the cacao is grown, harvested and processed

properly. Harvesting under-ripe cacao pods would result

in poor-quality yield because it won’t have developed all

its flavors and aromas and it will not continue to ripen

after harvest and not suitable for fermentation. On the

other hand, over-ripe cacao pods may germinate and

possibly will lead to fungal-infective, defective and

generate poor quality yields. The best way of harvesting

cacao pods is when it is about to ripe. The conventional

way of determining the ripeness of a cacao pod is by

manual tapping to get a hollow sound. Hollow sound will

indicate ripeness because the cacao beans are no longer

tightly packed inside the pod. This paper recommends an

approach to classify the ripeness of cacao using the

acoustic sensing technology.  The device will generate an

acoustic signal from cacao pods which was recorded for

acoustic signal analysis. Cepstral-based technique was

used for feature extraction and Support Vector Machine

(SVM) algorithm model and tested using nested cross

validation resulted in 94% mean test score.

Keywords—Acoustic Signal, Cacao, SVM, Cepstral-based

feature

I.  INTRODUCTION

Cacao (Theobroma cacao L.) a perennial tropical crop that

has been grown in the Philippines for thousands of years and

has widened recently, the cacao industry has been gaining

popularity on both the domestic and international markets.

Since 1970, the demand for cacao has nearly tripled,

expanding at a 3 percent annual rate, with China and India

growing at a 7.9 percent annual rate. It is grown from its seed

known as cocoa beans which can be used in the food,

cosmetics and pharmaceutical industries, and the positioning

of cacao as health food. Cocoa contributes significantly to the

economic growth of the cocoa- producing country’s

agricultural sector.

Harvesting is an essential initial procedure in cacao

processing to gain high-quality cacao beans. Unlike many of

the fruits in the Philippines, cacao pods grow all-year-round,

and even in the same season, the pods on the tree do not ripen

altogether. It is crucial to harvest immature or under-ripe

cocoa pods because it will not continue to ripen after harvest.

Under-ripe cacao pods are hard and do not contain

fermentable beans. Therefore, only those pods that are fully

matured are suited for harvest in order to get the highest yield

of high-quality cocoa beans.

Some farmers will harvest the cacao when the cacao pods

change color. The cacao pod's external wall color varies

depending on its variety, which makes it difficult to

accurately predict the cacao pod's maturity level from its

exterior appearance. For instance, the Criollo variety is

recognized as a superior quality, less bitter and more

aromatic. It will turn pale pink to dark red during maturity.

Forastero has a bitter taste, thus, often blended with superior

cocoas. It will turn from green to yellow during maturity [1].

However, not all ripe pods will completely change color

during their maturity. Furthermore, some knowledgeable

farmers employed the traditional method of detecting

ripeness by tapping the cocoa pods [2]; if the cocoa pod

makes a hollow sound, it is ripe because the cocoa beans are

no longer tightly packed inside the pod but rather are loose,

the pod is ready for picking [3]. According to the study of

Cooke and Rand, the mass, shape, and modulus of elasticity

of fruit all affect how loudly they vibrate. Using the

mathematical model for the modulus of elasticity, the product

of a constant is the frequency with the largest amplitude

measured in Hertz, mass in kilograms, and density in meter

cubed per kilogram [4]. Nourain, J. et al. created an acoustic

from the vibration detected by the accelerometer which was

transformed into an electric signal and was amplified and

filtered by a 3−3000 Hz band processing circuit [5]. However,

some studies used a compound of a fruit-bed, an impactor

(pendulum), sensing device, a laptop computer and software

to control the experimental setup and to analyze its results to

--- page 2 ---
acquire the acoustic impulse information [6]. Aside from the

accelerometer, some studies used microphone and

piezoelectric film sensors for other possibilities for dynamic

testing. They concluded that the sensor could detect the

firmness index of some tested fruits [7]. Additionally, some

researchers considered the water loss contributed a big effect

of the acoustic impulse response technique [8].

Several studies used machine learning in training the data.

Support Vector Method (SVM) was utilized in estimating the

ripeness of papaya which is measured 100% of the total

dataset for validation [9]. Moreover, SVM technique was

applied in creating five kinds of cocoa and were categorized

using an integrated methodology. Also, electronic tongue

(ET) and near-infrared spectroscopy (NIRS) were included in

addition to multivariate analysis [10]. For computer Vision

and audio processing, some popular feature extraction used

the combination of Recurrent Neural Networks (RNN) and

Convolutional Neural Networks (CNN). For instance, study

the ripeness of apples [8], melon [6][5][11] and papaya[9]. To

characterize the lung sound for the identification of associated

disease, cepstral-based technique was also used [12]. This

could be beneficial in providing new technology in the cacao

farm industry.

This study presents a method that uses an acoustic

collection device that was specifically fabricated to record

and process acoustic data of cacao pods, validating if

collected data can be used to classify the cacao pods.

Specifically, this study aims the following: (1) development

of an instrument that collects acoustic characteristics that

determine the cepstral statistical feature of ripe and unripe

cacao, (2) Compare and evaluate the cepstral statistical

feature of the two classes Ripe and Unripe (3) train and test

using Support Vector Machine- machine learning model for

cacao ripeness classification.

II. MATERIALS AND METHODS

The central concept of this study was the development of

an instrument that collects acoustic characteristics of ripe and

unripe cacao pods. Collected data will be used and analyzed

to develop a Support Vector Machine. The flowchart on how

the data was collected, processed and extracted the features

for the machine learning model training is shown in Figure 1.

Nested Cross Validation techniques were used to evaluate the

model.

Fig. 1. Flowchart of the Study

A. Instrumentation

A device was fabricated to fit the cacao pods. The acoustic sensor used a microphone connected via USB on the Raspberry Pi Model B+ (RaspPi) computer. The RaspPi was

the control unit of the mechanical impactor using a SG90

servo motor used to tap the pods uniformly, the acoustic

responses of the cacao pod were recorded and data were

stored in the computer as WAV file as shown Figure 2.

Fig. 2. Acoustic Signal Collection Flow

B.    Data Gathering

In gathering data, Thirty-six cacao pods were collected

from the farm. Identified cacao experts certified the quality of

cacao pods as ripe or unripe.  The eighteen unripe pods were

selected and perceived to ripen after two weeks and the other

eighteen cacao pods were collected fully-ripe. Each cacao

pod was placed on the instrument and mechanically tapped

four times. As shown in figure 3, data were recorded as

waveform audio file form in the computer every time the

cacao pod was tapped for three seconds. After processed in

figure 3, each cacao pod was sliced and opened for

verification of the expert as shown in figure 4.

Fig. 3. Cacao pod data acoustic recording and analysis.

Start

Instrumentation  Cross Validation

Data Gathering Model Output

Feature

Extraction Ripeness Classification

Model Training

Cacao

Pod

Mechanical

Excitation

Acoustic

Sensor

Data

Storage

--- page 3 ---
Fig. 4. (a). Ripe Cacao, (b.) Unripe Cacao

C.   Feature Extraction

During pre- processing, four of each cacao’s acoustic

signal were recorded using data mining procedure to extract

the statistical feature of each. The recorded data was analyzed

using librosa python audio analysis with a sampling rate of

44100 hertz and with an interval of three seconds and were

calculated using the Mel-frequency Cepstrum

Coefficients(MFCC) feature. Each Mel-frequency cepstral

coefficient was considered for the computation of the

standard deviation (SD) of the MFCC [12]. SD was computed

using equation 1. The x is the value computed in MFCC, μ is

the mean of MFCC and n is the number of coefficients.  Since

each cacao sample has four acoustic records, the mean of the

four recorded data was computed, standard deviation was

considered as Cepstral-based statistical feature of each cacao

pod as shown in figure 5.

ܦܵ ൌ ටቀ

σሺȁ௫ିఓȁሻమ

௡ ቁ                                  

Fig. 5. Algorithm for Cepstral-based statistical feature.

To visualize the gathered Cepstral-based statistical

feature(CSF) of data, a scatter plot of eighteen ripe cacao

pods and eighteen unripe cacao pods were computed using

cepstral-based statistical features as shown in figure 6. Green

color was identified as ripe and red for unripe. The x-axis of

the scatter plot is the number of samples and the y-axis the

level of cepstral-based statistical features.

Fig. 6. Scatter plot Ripe and Unripe cepstral-based statistical feature

D.   Model Training

To train the machine learning model Support Vector

Machine(SVM), the eighteen features extracted data of each

of the ripe and unripe cacao pods were used as training data,

in total thirty-six one dimensional array of data of class ripe

and unripe.  The Support Vector Machine used in this study

has a characteristic of a polynomial kernel and a two-

dimension input data; the training data was transformed into

a two-dimensional array using polynomial features of degree

two. The x-axis is the cepstral-based statistical feature while

the y-axis is the polynomial features as shown in figure 7.

This new transformed data is used to train the SVM model.

Fig. 7. Scatter plot of the transformed Cepstral-based statistical feature

This was implemented in a python environment using the

Sklearn library.

III. RESULTS AND DISCUSSION

In this section, the goal was to present and discuss the data

analysis process and to validate the methods described in

section II. First, the data collected in cepstral-based statistical

features of each ripe and unripe cacao as shown in figure 7,

was compared and analyzed to check if the ripe and unripe

data has significant difference, T-test was used as shown in

table 1.

WAV

file

Compute

MFCC

Compute

Statistical Feature

Standard

Deviation

--- page 4 ---
TABLE 1.  T-Test results of Ripe and Unripe data

Ripe  Unripe T-test

Mean SD Mean SD P-value

97.05 2.68 90.81 1.04 <0.01

The Mean of the Cepstral-based statistical features of ripe

and unripe is 97.05 and 90.81 with standard deviation(SD) of

2.68 and 1.04 and with a P-value of less than 0.01. This

presents the data from the extracted features of ripe cacao that

were spread out more than of the unripe cacao. It was shown

that there is a significant difference between the two dataset

collected. Also, this confirms that the cepstral-based

statistical features of ripe tend to have higher values

compared to unripe cacaos.    Furthermore, the data proved

that the instrument developed can capture the essential

acoustic response. In addition, the datasets can be used as

training data for a ripe and unripe classifier. To test, the

dataset used to train a machine learning model, Support

Vector Machine (SVM) was used to investigate the extracted

feature that can be used to classify cacao ripeness. Two

dimensional array of features was needed to train the model.

This was done in the data transformation in section II. The

Kernel used in the SVM model is the polynomial kernel with

Regularization Parameter C of one of these parameters

calculated using Nested Cross validation which calculates the

best parameters to be used to test the classifier. Figure 8

showed the separation of the hyperplane and the support

vectors of the trained model.

Fig. 8. SVM separating hyperplane and support vectors.

Aside from the computing the best parameter of SVM

model, Nested Cross validation was also used to validate and

test the performance of the model, because of small number

of datasets [13], validation and testing the model using K-fold

Cross validation and finding the best parameters in the SVM

model, The nested cross validation tested the kernels “linear”

,”poly” and “rbf”  with Regularization Parame ter C of  1, 5

,10 and 20 and k-fold splitting Strategy of 18 and resulted

that the best parameter to used is the “poly” kernel,

Regularization Parameter C of 1. The nested cross validation

also tested the classification performance of the model and

resulted in a mean test score of 94% accuracy. This suggests

that with a limited dataset, you can still train and test a

machine learning model that will result in a high

classification accuracy. As for overfitting, the nested cross

validation strategy can also be used [14] since the nested cross

validation incorporated a high k-fold value, each value in the

dataset was used as train and test set. This safeguards from

overfitting and unbiased results.  This was all done using the

Python Sklearn machine learning library.

IV. CONCLUSION AND FUTURE WORKS

The developed instrument in this study consists of a

microphone as an acoustic sensor and mechanical impactor

that is controlled by a computer can be used effectively to

collect acoustic characteristics. Based on the collected data,

cepstral statistics used the instrument and was analyzed using

T-test. The result has the mean and standard deviation of

97.05 and 2.68 for ripe and 09.81 and 1.04 in the unripe with

p-value of less than 0.01 which confirms that data collected

using the instrument has significant difference between

classes ripe and unripe. Furthermore, using the feature

extraction method as discussed in section II, the method can

effectively be used as an algorithm to extract cepstral

statistical features of ripe and unripe cacao pods. Support

Vector Machine Classifier was trained using the dataset

collected and tested using nested cross validation resulted in

a 94% mean test score. This concludes that cepstral statistical

features can be used as a basis in classifying ripe or unripe

Cacao pods. While this study yielded encouraging results, it

was recommended to investigate more on other cepstral

statistical features like the mean instead of standard deviation

or both. It was also recommended to use additional datasets

during the experiment.

REFERENCES

[1] E. O. Afoakwa, “Cocoa bean composition and chocolate flavour

development,” Choc. Sci. Technol., pp. 80–101, 2016.

[2] D. Z. H. Arenga and J. C. Dela Cruz, “Ripeness classification o f

cocoa through acoustic sensing and machine learning,” HNICEM

2017 - 9th Int. Conf. Humanoid, Nanotechnology, Inf. Technol.

Commun. Control. Environ. Manag. , vol. 2018-Janua, pp. 1 –6,

2017.

[3] M. Apriyanto, “ Changes in Chemical Properties of Dreid Cocoa (

Theobroma cacao ) Beans during Fermentation ,” Int. J. Fermented

Foods, vol. 5, no. 1, p. 11, 2016.

[4] J. R. Cooke and R. H. Rand, “A Mathematical Study of Resonance

in Intact Fruits and Vegetables Using a S-Media Elastic Sphere

Model,” J. Agric. Eng. Res., pp. 141–157, 1973.

[5] N. Jamal, Y. Yi-bin, W. Jian-ping, R. A. O. Xiu-qin, and Y. U .

Chao-gang, “and finite element analysis *,” no. 6, pp. 483– 490,

2005.

[6] F. Khoshnam, “Acoustic Testing for Melon Fruit Ripeness

Evaluation during Diff erent Stages of Ripening,” vol . 80, no. 4,

pp. 197–204.

[7] A. H. Gómez, A. G. Pereira, and J. Wang, “Acoustic impulse

response potential to measure mandarin fruit ripeness during

storage Universidad Agraria de La Habana Fructuoso Rodríguez

Pérez,” no. May, 2015.

[8] S. Landahl , V. Van Linden, and J. De Baerdemaeker, “Dependence

of Stiffness of Apples On and Off the Tree on Their Maturity an d

Water Potential,” pp. 421–427, 2003.

[9] P. B. Bro, C. Rosenberger, H. Laurent, C. Gaete-Eastman, M.

--- page 5 ---
Fernández, and M. A. Moya- León, “A support vector machine as

an estimator of mountain papaya ripeness using resonant frequency

or frequency centroid,” IFIP Int. Fed. Inf. Process., vol. 217, pp.

335–344, 2006.

[10] E. Teye, X. Huang, J. Takrama, and G. Haiyang, “Integrating NIR

spectroscopy and electronic tongue together with chemometric

analysis for accurate classification of cocoa bean varieties,” J.

Food Process Eng., vol. 37, no. 6, pp. 560–566, 2014.

[11] M. Taniwaki, M. Tohro, and N. Sakurai, “Measurement of ripening

speed and determination of the optimum ripeness of melons by a

nondestructive acoustic vibration method,” Postharvest Biol.

Technol., vol. 56, no. 1, pp. 101–103, 2010.

[12] N. Sengupta and G. Saha, “Lung sound classification using

cepstral-based statistical features Lung sound classification u sing

cepstral-based statistical features,” no. June, 2016.

[13] A. Vabalas, E. Gowen, E. Poliakoff, and A. J. Casson, “Machine

learning algorithm validation with a limited sample size,” PLoS

One, vol. 14, no. 11, pp. 1–20, 2019.

[14] C. Beleites, U. Neugebauer, T. Bocklitz, C. Krafft, and J.  Popp,

“Sample size planning for classification models,” Anal. Chim.

Acta, vol. 760, no. June 2012, pp. 25–33, 2013.

[15] McFee, Brian, Colin Raffel, Dawen Liang, Daniel PW Ellis, Matt

McVicar, Eric Battenberg, and Oriol Nieto. “librosa: Audio and

music signal analysis in python.” In Proceedings of the 14th python

in science conference, pp. 18-25. 2015.

[16] Scikit-learn: Machine Learning in Python, Pedregosa et al., JMLR

12, pp. 2825-2830, 2011.

[17] D. Hunter, "Matplotlib: A 2D Graphics Environment", Comput ing

in Science & Engineering, vol. 9, no. 3, pp. 90-95, 2007.

[18] Harris, C.R., Millman, K.J., van der Walt, S.J. et al. Array

programming with NumPy. Nature 585, 357–362 (2020).