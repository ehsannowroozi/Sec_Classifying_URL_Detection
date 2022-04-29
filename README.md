# Sec_Classifying_URL_Detection
Secure Classifying for Malicious URLs Detection Against Adversarial Attack


Authors: [Ehsan Nowroozi](https://scholar.google.com/citations?user=C0bNkP8AAAAJ&hl=en), Abhishek, [Mohammadreza Mohammadi](https://scholar.google.com/citations?user=yGtuQv4AAAAJ&hl=en)[Mauro Conti](https://scholar.google.com/citations?user=0BcsOY8AAAAJ&hl=en)

2022-2023 
[Ehsan Nowroozi], Center of Excellence in Data Analytics (VERIM), Sabanci University, Istanbul
Turkey 34956; Faculty of Engineering and Natural Sciences, Sabanci University, Istanbul, Turkey; University of Padua, Department of Mathematics, Seurity and Privacy Research Group (SPRITZ), Italy. (ehsan.nowroozi@sabanciuniv.edu, nowroozi@math.unipd.it, ehsan.nowroozi65@gmail.com). Personal Website: www.enowroozi.com

[Abhishek], MNNIT Allahabad, Prayagraj-211004, India and University of Delhi-110007, Delhi, India. (abhishek1verma99@gmail.com)
         
[Mauro Conti], University of Padua, Department of Mathematics, Seurity and Privacy Research Group (SPRITZ), Italy. (mauro.conti@unipd.it)


This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

If you are using this software, please cite from [***](****). 

****

Introduction
------------
The goal of our research is to identify malicious advertisement URLs and to apply adversarial attack on ensembles. We extract lexical and web-scrapped features from using python code. And then 4 machine learning algorithms are applied for classification process and then used the K-Means clustering for the visual understanding. We check the vulnerability of the models by the adversarial examples. We applied Zeroth Order Optimization adversarial attack on the models and compute the attack accuracy.


Datasets
--------
Datasets are taken from different sources avlailable on internet. We have considered 12 different datasets which consists of 6 malicious and 6 benign URLs. The dataset includes about 3980870 URLs. We extracted the 89 lexical and web scrapped features for the further task. Original dataset URLs are available [Dropbox](https://www.dropbox.com/s/r90hufaok1fgn6f/Original%20Datasets.zip?dl=0)

Resources
--------------
Our techniques requires PL   : PYTHON (VERSION 2.7.17), IDE  : PyCharm Community Edition
numpy #version 1.19.5
pandas #version 1.1.5
seaborn

Sample Commands 
---------------
In all the datasets, the benign URL is denoted by '0' and malicious URL is denoted by '1'. 
Example: 
http://www.exampledomain.com/urlpath/       '0'

http://www.exampledomain.com/urlpath1/      '1'

The URL label is either +1 (Malicious) or 0 (Benign).


Training the classifiers.
-------------------------
The classifiers are trained with the 6 extracted datasets and then tested. The four models random forest, adaboost, gradient boost and xgboost are the four classifiers and these are trained on the 6 datasets. We have made also applied the testing and training on different mismatched datasets. The code for them are also given. The different parameters of the model are adjusted for the best results.
It's been identified that a competent adversarial URL generating system can come up with URLs that can get past ML classifiers at the rate of one every 20 seconds or so. This makes current malicious URL detection systems insufficient.
We overcome this using a Random Forest Classifier with adversarial training to counter adversarial attacks that works with an accuracy of approximately 96 percent.

In any case, such an increase in the accuracy, and subsequently the model should be improved upon in that aspect.

The solution to be worked on is to build a GAN on the URL dataset and separate the discriminator in the end, which will be our result; rather than our current approach here which was to use the ART toolbox to attack once and using that data to train. Also, if we want to merely improve our current approach we need to attempt a weighted ML classifier aimed to reduce misclassifications, rather than use an ensemble algorithm (which has generally reduced misclassifications)


Output of the Classifiers
-------------------------
The sample output of the classification result is as below.
Example:
accuracy of train phase is 99.6500
accuracy of test phase is 99.3500
Mean Squre Error - train 0.0000
Mean Squre Error - test 0.0050

Metrics
-------------------------
Test accuracy score 99.6500
Test Recall 99.0610
Test Precision 99.1500
Test F1 Score 99.5283
Test F2 Score 99.2474

TPR, TNR, FPR, FNR
--------------------------
TPR 0.9957
TNR 0.9911
FPR 0.0089
FNR 0.0043


Please download the following packages for the implementation of ZOO attack:
-----------------------------------------------------------------------------
from sklearn.ensemble import GradientBoostingClassifier
from matplotlib import pyplot as plt
import art#fully initialise module
from art.estimators.classification import SklearnClassifier
from art.attacks.evasion import ZooAttack

Please download the following packages for training the classifiers:
------------------------------------------------------------------------------
import numpy
import pandas
import seaborn
import matplotlib.pyplot
sklearn
sklearn.ensembles

For clustering:
import pandas
import numpy 
import matplotlib.pyplot
import mglearn
from sklearn.cluster





