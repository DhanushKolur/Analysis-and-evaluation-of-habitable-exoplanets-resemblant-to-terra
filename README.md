“Analysis and evaluation of habitable exoplanets resemblant to terra”
        
ABSTRACT
Planet identification has been done by cosmology experts and researchers using sophisticated equipment
for several decades. This pattern has shifted with the introduction of computer technologies and the
availability of satellite data from space missions. NASA’s Exoplanet Exploration program, for example, 
has given humanity massive volumes of data about celestial objects to use in space exploration. The 
Kepler mission is an example of a mission of interest. Since the project began in 2007, nearly 4000 
transiting exoplanets have been found, recognized, and cataloged. Its primary goal was to investigate 
planets and planetary systems. It has supplied us with a large database of findings that may be used to
calculate planet occurrence rates as a function of an object's properties such as size, insolation flux, star
type, and orbital period. This data is catalogued in the Cumulative Kepler Object of Information dataset, 
which is accessible for public use on NASA's exoplanet repository. Four fundamental models have been 
compared. Support Vector Machines, Random Forest Classifiers, AdaBoost, and Deep Neural Networks. 
The above-mentioned models will be used to analyze exoplanets and categorize them.
Table of Contents
ABSTRACT………………………………………………
ACKNOWLEFGEMENT………………………………..
CONTENTS……………………………………………….
LIST OF FIGURES……………………………………….
LIST OF TABLES………………………………………...
CHAPTER 1: INTRODUCTION………………………...
General Introduction……………………………………… 01
1.1 Existing System…………………………………… 02
1.2 Proposed System………………………………… 03
1.3 Motivation………………………………………… 04
1.4 Objectives…………………………………………. 05
1.5 Key Features………………………………………. 05
1.6 Organization of the report………………………… 06
CHAPTER 2: LITERATURE SURVEY………………...
2.1 Habitability of exoplanets using deep learning……. 07
2.2 Searching for exoplanets using artificial intelligence… 07
2.3 Habitability classification of exoplanets………….. 07
2.4 Nigraha: Machine-learning-based to identify Exoplanets… 07
2.5 Habitability of Exoplanets using Deep learning....................... 08
2.6 The ML Pipeline for Exoplanet Grouping................................ 08
CHAPTER 3: SYSTEM REQUIREMENTS AND SPECIFICATION
3.1 System Requirements ............................................................... 09
3.2 Hardware Requirements ........................................................... 09
3.3 Platform..................................................................................... 09
CHAPTER 4: SYSTEM DESIGN…………………………………
4.1 Input and output design............................................................ 10
4.2 System Architecture…............................................................. 11
4.3 System Contents……………………………………….. 12
4.4 Object Oriented design ............................................................ 12
4.4.1 Flowchart………………………………………… 12
4.4.2 Use case Diagram…………………………………… 13
4.4.3 Sequence flow Diagram……………………………… 15
CHAPTER 5: IMPLEMENTATION………………………………..
5.1 Module splitup ........................................................................ 16
5.1.1 Data pre-processing ………………………………… 16
5.1.2 Feature Correlation and variance…………………… 16
5.1.3 Evaluation metrics and cross validation........................... 17
5.1.4 Classification models……………………………….. 17
5.2. Implementation and output……………………………… 18
5.2.1 K-means clustering................................................... 18
5.2.2 Agglomerative clustering………………………… 20
5.2.3 Random –Forest Classifier………………………. 22
5.2.4 Support Vector Classifier………………………... 25
5.2.4 Adaboost………………………………………… 28
5.3. Sample Code………………………………………… 32
5.3.1 Visualization……………………………………. 32
5.3.2 K-means clustering and agglomerative.................. 53
5.3.3 SVM and random forest and adaboost…………… 54
 CONCLUSION…………………………………………….... 77
 FUTURE ENANCEMENTS………………………………. 78
 REFERENCES………………………………………………. 79 
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 1
CHAPTER 1
INTRODUCTION
General Introduction
For ages, astronomy has fuelled our inquisition and has made us question and ponder over the
mystery surrounding our existence and role in this universe. It is natural human tendency to
question if the celestial objects that we know of are planets or not considering the fact that we
inhabit one - and may soon need to find another. This question has stimulated the minds of
researchers for centuries and the task of identifying exoplanets, which are essentially planets
apart from the ones we know, way beyond our solar system, and has led to novel discoveries.
Until now, this has been a time-intensive and tiring task, reserved only for astronomical experts
with substantial domain knowledge and included the use of specialized equipment. These
experts study images collected by satellite-based telescopes like the Hubble. With the launch
of a whole new generation of modern astronomy and technologically advanced telescopes and
satellites such as the Kepler, a new door has opened up for exoplanet exploration with the
ultimate goal being to automate the analysis of scientific observations and data generation
pertaining to exoplanet identification. These satellites and telescopes apart from taking images,
also process them using astronomical and mathematical techniques to produce data with a
variety of features for identifying these exoplanets. This data has been made publicly available
and democratized the once arduous task of exoplanet exploration among data scientists,
engineers and statisticians alike. Modern intelligent algorithms and techniques such as Machine
Learning and Deep Learning can be applied to exoplanet data to detect overlooked and
misclassified exoplanets and objects of interests in data archives or automate the pipeline. The
models explored include Support Vector Machines, Random Forest Classification, AdaBoost
and Deep Neural Networks. They were used to classify objects found in the Kepler Cumulative
Object of Interest [2] (KCOI) table. The KCOI table contains 50 features recorded from Kepler
data. This data has been pre-processed to retain the most important features, 19 to be specific.
Finally, models have been fit on this data and eventually used to assign the probability for an
object in the KCOI table being an exoplanet. Traditional methods of discovery such as
obtaining and analysing images of distant stars are now outdated. A digital transformation in
astronomy is underway. As opposed to satellite based telescopes from the past, the primary
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 2
function of these satellites is to record and process a variety of data, not just images. We now
find various powerful and state-ofthe-art Machine Learning techniques at our disposal to look
for exoplanets. As this data has been made publicly available, this makes the task all the more
easy. The Kepler Space Telescope was launched by NASA in 2009. To date, it has been the
most successful telescope to aid the discovery of exoplanets. It has identified several thousand
objects of interest, with over 4300 of them confirmed exoplanets. The catalogue has a high
reliability rate, averaging 85%-90% over the radius plane. It continues to improve as followup observations continue. While Kepler has been officially decommissioned as of October
2018 as it ran out of fuel, the statistical data it has accumulated is capable of providing insights
for new exoplanet discoveries for years to come.
1.1 Existing system
Given the complexities of analysing planetary habitability, there is no way to clearly decide
on exoplanet habitability classes, kinds, and so on at this time. Travel Photometry also has a
few key drawbacks as a result of the cosmologist's point of view and the discovered transit
value. Only approximately 10% of planets with short orbital periods have such an
arrangement, and decreases for planets with longer orbital periods are due to the trip
photometry caveat. The proficiency of the algorithm used in the machine learning model tends
to lower due to the varying sets of data of each and every exoplanet detected due to the
characteristics exhibited by the exoplanet during its detection, such as obscuring image due to
change in brightness, change in estimated transit period, and so on. Grading method of
discovering exoplanets, of a kind that taking and examining images of remote stars, have
become concentrated. The field of astronomy is undergoing a digital transformation. Unlike
earlier satellite-based surveys, the primary objective of artificial satellite is to obtain, reserve,
and analyse a wide range of statistics in order to categorize exoplanets. Exploring Exoplanet
Populations with NASA’s Kepler Mission’ reports on the progress made by Kepler in
measuring the prevalence of exoplanets orbiting within 1 AU of their host stars. This
strengthens NASA’s long-term goal of finding habitable planets beyond our solar system. She
talks about exoplanet confirmation and characterization and the requirements needed for a
reliable exoplanet occurrence rate. Another paper titled ‘Advances in Exoplanet Science from
Kepler’ [4] by Jack J. Lissauer et. al discusses the highlights of the Kepler mission. While the
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 3
two papers discuss the highlights of the mission, they fail to talk about any exoplanet detection
methods. ‘Identifying Exoplanets with Deep Learning. Convolutional Neural Networks
(CNNs) are used to predict if signals caused by either astrophysical or instrumental
phenomena correspond to an exoplanet. The model was able to correctly classify plausible
planet signals on the test set 98.8% of the time. Additionally, they validate two new exoplanets
that are identified, with high confidence by their model. This paper explores Deep Learning
approaches but does not compare its performance with other Machine Learning models.
‘Transiting Exoplanet Discovery Using Machine Learning Techniques’ [6] propose a model
to create synthetic datasets of light curves. Several Machine Learning algorithms are used to
identify transiting exoplanets. They conclude that multi-resolution analysis in the timefrequency domain improves exoplanet signal identification, due to the various characteristics
of light curves and transiting planet signals. A Gaussian process classifier reinforced by other
models is used to perform probabilistic exoplanet validation by accounting for prior
probabilities for possible false positives. This paper identifies the caveats against the use of
single-method planet validation techniques and cautions against it. ‘False Positive
Probabilities for all Kepler Objects of Interest: 1284 newly validated and 428 likely false
positives. This presents astrophysical false positive probability calculations for every recorded
Kepler Object of Interest. It was the first large-scale demonstration of a fully automated
transiting exoplanet validation procedure.
1.2 Proposed System
In our proposed system, machine learning algorithms plays vital role. Machine learning
algorithms are majorly classified into three divisions: namely, Regression, clustering and
classification. The Classification method is a Supervised Learning approach that uses training
data to identify the category of fresh observations. In classification the given set of the data is
categorized into classes. These classes are often named as target, label or categories.
Classification is predictive modelling that operates in a supervised learning environment.
Different machine learning classification algorithms may be understood depending on the
nature of the dependant variable. This project mainly focuses on sorting the Objects of Interest
as "FALSE POSITIVE" or "CONFIRMED" exoplanets. In the case where the satellite
manifests an item wrongly then Nasa uses the term “FALSE POSITIVE “. Here we refuse to
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 4
take in consideration the observations which are labelled as CANDIDATE, because Nasa is
yet to name them and hence, we are not aware about them. Data pre-processing refers to the
actions required to alter or encode data so that it may be easily interpreted by a machine. Once
after the completion of the data pre-processing stage, we verify all the characteristics are on
the same scale. The main advantage of this step is that, after the verification of all the
characteristics, it helps to improve the performance as well as reduces the computing effort
which is required by the models. Implementing machine learning (ML) that is classification
models for the exoplanets that are Support Vector Machine (S V M), Random Forest, Adaptive
Boost (ADA-BOOST), K-Means Clustering (KMC), Agglomerative Clustering. The imitation
will foreshow the tenantable of exoplanets by Kepler’s cumulative object of interest raw data.
1.3.1 Data Pre-Processing.
1.3.2 Feature Co-Relation and Variance.
1.3.3 Evaluation Metrics and Cross-Validation.
1.3.4 Classification Models.
1.3 Motivation
Astronomy is one of human civilization’s oldest natural sciences. Throughout history, astronomy has
influenced religion, guided explorers, defined food production schedules and fuelled philosophical
questions surrounding our very existence and role in the universe. A natural extension of our curiosity
with the stars is to question if there is another planet, in another solar system capable of supporting
life. The answer to this question has been pondered and researched for hundreds of years. The task
of identifying planets outside of our solar system, known as exoplanets, leads to genuinely novel
discoveries. Exoplanet identification has traditionally been a time-intensive task reserved for highlytrained, educated experts with access to specialized—and usually expensive—equipment. These
experts relied upon their education, intelligence, diligence, and team knowledge in their painstaking
search for exoplanets using images collected by terrestrial observatories and satellite-based
telescopes, such as Hubble which led us to a keen interest in this category. A new era has dawned in
the hunt for exoplanets however; a new generation of modern satellites, such as Kepler, have been
launched in recent years with the goal of partially automating scientific observations and data
generation related to exoplanet identification. These satellites are engineered to not only take
pictures but to process those images using proven astronomical techniques to produce a vast
collection data with the right variety of features for identifying exoplanets. We can interrogate this
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 5
data to help confirm if an object of interest they have discovered is indeed an exoplanet.
1.4 Objective
➢ The project’s main goals are as follows:
• The accessibility of data has led to categorizing exoplanets to the world with the vision
and power to communicate and make sense of these learning models to categorize the
Exo-Planets.
• The algorithms will forecast the liveable exoplanets by the KCOI dataset. The machinelearning models can be put in for the latest telescope with upgraded technology i.e.,
James Webb Telescope to analyse the exoplanets.
1.4 Scope of the project
• The Exoplanet Exploration Program is guiding humankind on an unprecedented size
and purpose quest. The major aim of the initiative is to find and distinguish the Terralike planets encircling nearby stars. The goals are planned and evaluated to build on
one another’s triumphs, with each taking a crucial pace towards locating habitable
planets and signs of life outside our zone.
• • The satellite information is so widely available, that identifying planets has become a
challenge for everyone who can design and assess machine learning models. This study
employs a number of classification approaches and datasets to determine the chance
that observation is an exo-planet.
• The algorithms will foresee single planetary transits in the KCOI dataset using
replicated training data. The simulated data is comparable to an authentic planetary
search survey.
•
1.5 Key Features
• NASA’s focus lay on exploring planets and planetary systems.
• It has traditionally been a time-intensive task reserved for domain experts with access
to specialized equipment.
• These experts study images collected by satellite-based telescopes like the Hubble.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 6
• A new generation of modern satellites such as Kepler has opened the door for
exoplanet exploration
• New technologies are trying to partially automate scientific observations.
1.6 Organization of the Project Report
The project report has been broadly divided into following chapters: -
Chapter 1 gives Existing System, Proposed System, Project Motivation, Problem
Objectives, Key Features.
Chapter 2 discuss about Literature Survey.
Chapter 3 gives the System Requirement specifications of the project.
Chapter 4 gives the System Design of the project.
Chapter 5 gives the implementation details of the project.
Chapter 6 gives the types of tests carried out in project.
Chapter 7 gives the Results derived along with the suggestions for future enhancements.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 7
CHAPTER 2
LITERATURE SURVEY
Literature Survey is an important phase in the software development life cycle as we acquire
the necessary knowledge and skills required to handle or develop a project during the phase.
2.1 Habitability of exoplanets using deep learning: Authored by Rutuja Jagtap; Unzela
Inamdar; Shivani Dere; Maziya Fatima; Nikhilkumar B Shardoor(2013):
The efficiency of several machine learning algorithms in categorizing exoplanets into thermal
habitability classes and describing them based on probable habitability is discussed in this
research. They proposed developing and deploying a machine learning model to automate
Kepler cumulative object of interest data categorization. Deep learning techniques were used
to achieve the key goals of exoplanet categorization and discovery.
2.2 Searching for exoplanets using artificial intelligence : Authored by Kyle A.Pearson,
Leon Palafox, and Caitlin A.Griffit(2017) :
They introduced a new approach for finding exoplanet candidates in massive planetary search
programs that, unlike current methods, make use of a neural network. Neural networks, also
known as deep learning or deep nets, are intended to provide a computer with insight into a
specific problem by teaching it to recognise patterns.
2.3 Habitability classification of exoplanets : A machine learning insight- Authored by
Suryoday Basak;Archana Mathur (2018):
Jayanth Murthy. In this paper the authors have explored the efficiency of the machine learning
in specifying the exoplanets into various different class. They conducted a deep investigation
of the data format and purpose approaches that may be utilised to efficiently categorise fresh
planetary samples. The data utilised in this paper came from the Puerto Rico Planetary
Habitability Laboratory's Exoplanets Catalog. Methods for data exploration and
experimentation culminate in the creation of a generic data methodology and a collection of
best practises that can be utilised for exploratory data analysis and experiments.
2.4 Nigraha: Machine-learning-based-pipeline to identify and evaluate plante candidates
from TESS(2019):
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 8
This paper is authored by Sriram Rao,Ashish Mahabal ,Niyanth Rao and Cauligi Raghavendra
.The transiting exoplanet survey spacecraft has already been active for little more than two
years, once covering both the northern and southern hemispheres.According to this paper, they
have used the fusion of the transit finding , supervised machine learning , and the detailed
finding to identify the new planets which were missed by the prior searches . In this paper They
have suggested methods for increasing yield by strengthening some of the processes where we
have been conservative and eliminated items due to a lack of datum or two. For categorising
light curves, various conventional machine learning-based approaches such as decision trees,
k closest neighbours, and random forests have been investigated.. They’ve also explored the
CNNs usage for the classification of TESS light curves to search for the exoplanet.
2.5 Title: Habitability of Exoplanets using Deep learning( 2021) :
In this work, the researchers present a deep learning technique for discovering and
categorizing planets predicated on their habitable behaviors. The ASTRONET deep learning
model predicts astronomical anomalies by classifying but whether or not the newly found
planet is habitable. Using a Deep Learning algorithm to predict the habitability of exoplanets:
In this context, liveable refers to the characteristic of having distinguishing traits to being
acceptable, ample to reside in. Exoplanets' density, boundary, curiosity, orbital bearing,
importance, and conductivity together be used to indicate liveability. The proposed
ASTRONET framework searches and detects possibly habitable exoplanets using a range of
planet and star attributes.
2.6 Title: The ML Pipeline for Exoplanet Grouping( 2019) :
They suggested improved machine learning version to categorise and operating KCOI datasets.
To create a superior grouping style, the "K N N", "Random Forest", and "S V M form" were
utilized, and its specificity, accuracy, and memory were tested and evaluated. For model
deployment, Flask APT and Azure Cloud were used. It includes a thorough machine learning
pipeline: in order to resolve flaws, developers must assure error-free data, train models, and
test them. The Random Forest identifies the width, transition factors, and balanced angle as
perhaps the top critical characteristics for detecting objects of interest.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 9
CHAPTER 3
SYSTEM REQUIREMENTS AND SPECIFICATION
A Software requirements and specification (SRS) is an important part of the software lifecycle
and is an input for the design phase. It is a basis for the validation of final deliverable outcome.
Any changes made to the requirement in the future will have to go through a format change
approval process. The detail of the requirement specification document is as below
3.1 Software requirements
OS : Windows 10 or Ubuntu 20.04 LTS
Compiler : PyCharm or Anaconda
Table 3.1.1-Software requirements
3.2 Hardware requirements
Processor : Intel core i3 11th gen or AMD K-5.
Processor speed : 2.60 GHz
RAM : 8 GB
Display resolution : 1366*768
Table 3.2.1-Hardware requirements
3.3 Platform
The recommending engine has been tested and will be integrated utilizing Goggle
Collab and Jupyter notebook. Based on the package requirement exhortation engine or
recommendation model is presented by means of cloud IDE or real-time IDE.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 10
CHAPTER 4
SYSTEM DESIGN
The purpose of design is to plan the solution for the problem analysed in analysis phase. This
phase is the first step in moving from problem to solution domain. The design of system is
perhaps the most critical factor affecting the quality of the software and has a major impact on
the later phases, testing and maintenance. This chapter discusses the high level design and
detailed design of the project.
4.1 Input and Output Design
This procedure of specifying a system's architecture, segments, terminals, and records in
sequence for it to suit its unique demands is based on the system design. The developed
system is essential for creating the outline and developing the product. The fundamental
purpose of this research is to provide the end user with the system's required capabilities.
The user must obtain the anticipated outcome in a timely and accurate manner.
Fig 4.1.1- I/O Design.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 11
4.2 System Architecture
The model architecture is as follows:
Fig. 4.2.1 System Architecture
1. Training and Testing data:
The training dataset is the first collection of data needed to train ML methods. ML
methods are taught how to make predictions or complete a task using training
samples. The test set is a set of data used to evaluate the performance of the model
using a performance index. It's crucial that none of the information from the training
set make it into the test set. If the testing set comprises instances from the training
dataset, determine if the algorithm has learned to generalize from the training set.
2. ML models:
The Machine Learning style output is a quantitative description of reality
phenomenon this is employed in the coaching procedure.
3. Evaluation and Prediction:
The technique used to assess the correctness of a structure’s expectations is known
as model evaluation. To accomplish this, employing a new and independent dataset
to monitor the efficiency of the freshly trained model is necessary. The annotated data
will be compared to the predictions of the model. by use several metric assessors such
as the F1-Score, Confusion Matrix, and so on.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 12
4.3 System Contents
Data Collection- A KOI is a star discovered by the Kepler area observatory as having
one or more transiting planets. The Kepler cumulative object of interest information
contains KOIs extracted from the Kepler Input Catalog's specialized record of 1, 50,000
stars.
Data Pre-processing- Pre-processing issettled priorto coaching and evaluating the facts
so that the data technologist can effortlessly resolve the information and implement thistowards
theMLmethods.So, we are allowed to receive a faultlesssolution.
Dataset Splitting: The information should be separated to two divisions:
Training, Testing.
Model Training: Following the advanced-clarifying facts, it is translated into coach and
evaluate the information. The method will accessthe information and bring forth an result that
will enable usto analyze the exactness ofsurvey and assorting the exoplanets.
Model evaluation and testing: Method for establishing an uncomplicated method
which is made possible to certain a value fast and with high precision rate. This is
further attained by model regulating and trial each model discretely for excellent result.
4.4 Object Oriented Design
Object-Oriented design is the process of planning a system of interacting objects for
the purpose of solving a software problem.
4.4.1 FLOWCHART
A flowchart is a type of diagram that represents a workflow or process. A flowchart
can also be defined as a diagrammatic representation of an algorithm, a step-by-step approach
to solving a task.
The flowchart shows the steps as boxes of various kinds, and their order by connecting the
boxes with arrows. This diagrammatic representation illustrates a solution model to a
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 13
given problem. Flowcharts are used in analysing, designing, documenting or managing a
process or program in various fields
Fig : Flow Chart
4.4.2 Use Case Diagram
use case diagram in the Unified Modelling Language (UML) is a type of behavioural diagram
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 14
defined by and created from a Use-case analysis. Its purpose is to present a graphical
overview of the functionality provided by a system in terms of actors, their goals (represented
as use cases), and any dependencies between those use cases. The main purpose of a use case
diagram is to show what system functions are performed for which actor. Roles of the actors
in the system can be depicted.
Fig Use Case Diagram
4.4.3 Sequence Flow Diagram
A sequence diagram or system sequence diagram (SSD) shows process interactions arranged
in time sequence in the field of software engineering. It depicts the processes involved and the
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 15
sequence of messages exchanged between the processes needed to carry out the functionality.
Sequence diagrams are typically associated with use case realizations in the 4+1 architectural
view model of the system under development. Sequence diagrams are sometimes called event
diagrams or event scenarios.
Fig Sequence Diagram
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 16
CHAPTER 5
Module Split Up and Implementation
5.1 Module Split-up
“KCOI” datasets have certain limitations where the data is absurd which is updated on Kepler
Telescope’s observation. It underdone dataset derived directly firsthand from “Kepler’s
observations” after labeling. Hence carries now no longer handiest lacking values however
additionally a massive range of unnecessary columns. Some of those may be skipped due to
the fact they're ID properties. However, the majority is essential to our have a look at and has
to be stuffed incorrectly. This degree assists us to modify the overall performance of our version
and doing away with redundant functions that carry no fee to our purpose.
5.1.1 Data Pre-processing
• By observing the columns that have missing values. We observe that though quite
a lot of these columns do contain missing values, most of these missing values
correspond to the errors associated with attribute values.
• We finalize the data pre-processing step by standardizing our data, to ensure all
attributes are on the same scale. This increases performance and also decreases the
computational effort required by the models, thus speeding up the process of
classification.
5.1.2 Feature Correlation and Variance
• To reduce redundancy in the number of attributes chosen, the correlation between
the attributes, and observe the results. While there is a correlation present between
the attributes picked in our study, most of the correlations are not of a high order.
• Only a few attributes exhibit a high correlation with the dependent variable. Most
attributes are observed to have only a medium or low correlation.
5.1.3 Evaluation Metrics and Cross-Validation
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 17
• To counter the imbalance of the dataset, we propose different evaluation metrics,
which take into account the imbalance.
• These include the F1 Score, Cohen Kappa score, Balanced Accuracy Score, and
finally the Confusion Matrix.
5.1.4 Classification Models
• To observe how different classifiers tackle the issue of existing model, we propose
to use classifiers working on different approaches.
• Those are traditional classifiers like the SVM, Bagging , Boosting Classifiers like
the AdaBoost and finally Neural Network.
• Finally perform Grid Search on each classifier with different values for its
hyperparameters to choose the optimum set of values that provide maximum
performance.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 18
5.2 Implementation and Outputs
5.2.1 K Means Clustering :
The K-means clustering set of rules computes centroids and repeats till the finest
centroid is determined. It is presumptively regarded what number of clusters there are.
It is likewise referred to as the flat clustering set of rules. The variety of clusters
determined from records via way of means of the approach is denoted via way of means
of the letter ‘K’ in K-means. In this approach, records factors are assigned to clusters
in one of these manner that the sum of the squared distances among the records factors
and the centroid is as small as possible. It is vital to word that decreased range inside
clusters results in extra equal records factors in the identical cluster.
Fig. K means clustering
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 19
Fig. elbow for K means Clustering
Fig. K Means OUTPUT
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 20
5.2.2 Agglomerative clustering:
“Agglomerative clustering is the maximum not unusual place form of hierarchical
clustering used to organize items in clusters primarily based totally on their similarity. It's
additionally called AGNES (Agglomerative Nesting).Agglomerative clustering makes use of
a bottom-up approach, in which every statistics factor begins off evolved in its very own
cluster. These clusters are then joined greedily, through taking the two maximum comparable
clusters collectively and merging them. Divisive clustering makes use of a top-down approach,
in which all statistics factors begin withinside the identical cluster”.
 Fig. Agglomerative Clustering
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 21
 Fig. Dendrogram
 Fig. elbow for Agglomerative clustering
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 22
 Fig. AMC OUTPUT
5.2.3 Random Forest Classifier (RFC):
“A random forest is a meta estimator that makes use of averaging to enhance projected
accuracy and manipulate over-becoming through becoming numerous decision tree
classifiers on awesome sub-samples of a dataset”.” Each Decision Tree within side the
Random Forest has the same hyperparameters and can be changed accordingly.
Because the Random Forest is so strong, it takes much less fine-tuning to create a
correct model”.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 23
Fig. Workflow of RFC
Evaluation Metric (EM_rfc) :
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 24
Fig . EM for RFC with Error Attributes
Cross-Validation (CV):
Fig. CV for RFC with Non Error Attributes
Fig. RFC OUTPUT 1
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 25
Fig. RFC OUTPUT 2
5.2.4 Support Vector Classifier (SVC):
"SVCs are methods for supervised learning that can be applied to classification,
regression, and outlier detection. Both dense and sparse sample vectors are acceptable
inputs for support vector machines in sci-kit-learn. We employ a Support Vector
Classifier (SVC) as our subsequent classifier. We utilize the R.B.F kernel and Gaussian
to alter the dimensionality of the data because it is not linearly separable. This might
aid in model optimization”.
( SVC workflow)
Fig. Non-Linear separable values
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 26
Fig. EM for SVC
Cross-Validation (CV):
Fig. CV for SVC with Non Error Attributes
Discrimination_Threshold (Dist_t):
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 27
Fig. Dist_t of SVC
FIG. SVM OUTPUT 1
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 28
FIG. SVM OUTPUT 2
5.2.5 ADA_Boost:
“This classifier is a meta-estimator that suits a classifier at the authentic dataset first,
then multiple copies of the identical dataset with the weights of poorly labeled times
modified such that destiny classifiers focus on tough circumstances.” If the present day
classifier predicts an instance wrong, the load for the subsequent classifier is increased,
and inverversly. However, due to the fact this makes it specifically at risk of overfitting,
we determined to use cross-validation to common out the results. AdaBoost is
finetuned. Because AdaBoost has its personal hyperparameters (in addition to the
Decision Tree hyperparameters), we deal with tweaking the AdaBoost classifier and
merely adjust the intensity of the selection tree”.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 29
Fig. 21. Ada_boost workflow
Evaluation Metric (EM):
Fig. EM for ADA_Boost
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 30
Cross-Validation (CV):
Fig. CV for ADA_Boost with Non Error Attributes
Discrimination_Threshold (Dist_t):
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 31
Fig. 24. Dist_t of ADA_Boost
FIG. ADA_BOOST OUTPUT 1
FIG. ADA_BOOST OUTPUT 2
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 32
5.3 Sample Code
5.3.1 Visulization
{
"cells": [
{
"cell_type": "markdown",
"metadata": {
"colab_type": "text",
"id": "view-in-github"
},
"source": [
"<a href=\"https://colab.research.google.com/github/aditeyabaral/kepler-exoplanetanalysis/blob/master/src/Data_Cleaning.ipynb\" target=\"_parent\"><img
src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In
Colab\"/></a>"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "UR20VBJPuSj0"
},
"source": [
"# Importing Libraries"
]
},
{
"cell_type": "code",
"execution_count": 1,
"metadata": {
"id": "BR3Rp5z1uSj3"
},
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 33
"outputs": [],
"source": [
"import pandas as pd\n",
"import numpy as np\n",
"import matplotlib.pyplot as plt\n",
"import pprint"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "lH2XW_hNuSj_"
},
"source": [
"# Initialising libraires"
]
},
{
"cell_type": "code",
"execution_count": 2,
"metadata": {
"id": "r2ybFWuluSkD"
},
"outputs": [],
"source": [
"pp = pprint.PrettyPrinter(indent = 3)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "SENGpu_xuSkK"
},
"source": [
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 34
"# Loading DataFrame"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "fk9GB07CuSkM"
},
"source": [
"[Dataset URL](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)<br>\n",
"[Link to
Metadata](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.ht
ml)<br>\n",
"[Column Name
Metadata](https://exoplanetarchive.ipac.caltech.edu/docs/API_keplerstellar_columns.html
)"
]
},
{
"cell_type": "code",
"execution_count": 3,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 244
},
"id": "wJzdrqMnuSkN",
"outputId": "9b5894d2-9d18-4ec0-80a5-e9e17e5ccb2a"
},
"outputs": [
{
"name": "stdout",
"output_type": "stream",
"text": [
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 35
"(9564, 50)\n"
]
},
{
"data": {
"text/html": [
"<div>\n",
"<style scoped>\n",
" .dataframe tbody tr th:only-of-type {\n",
" vertical-align: middle;\n",
" }\n",
"\n",
" .dataframe tbody tr th {\n",
" vertical-align: top;\n",
" }\n",
"\n",
" .dataframe thead th {\n",
" text-align: right;\n",
" }\n",
"</style>\n",
"<table border=\"1\" class=\"dataframe\">\n",
" <thead>\n",
" <tr style=\"text-align: right;\">\n",
" <th></th>\n",
" <th>rowid</th>\n",
" <th>kepid</th>\n",
" <th>kepoi_name</th>\n",
" <th>kepler_name</th>\n",
" <th>koi_disposition</th>\n",
" <th>koi_pdisposition</th>\n",
" <th>koi_score</th>\n",
" <th>koi_fpflag_nt</th>\n",
" <th>koi_fpflag_ss</th>\n",
" <th>koi_fpflag_co</th>\n",
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 36
" <th>...</th>\n",
" <th>koi_steff_err2</th>\n",
" <th>koi_slogg</th>\n",
" <th>koi_slogg_err1</th>\n",
" <th>koi_slogg_err2</th>\n",
" <th>koi_srad</th>\n",
" <th>koi_srad_err1</th>\n",
" <th>koi_srad_err2</th>\n",
" <th>ra</th>\n",
" <th>dec</th>\n",
" <th>koi_kepmag</th>\n",
" </tr>\n",
" </thead>\n",
" <tbody>\n",
" <tr>\n",
" <th>0</th>\n",
" <td>1</td>\n",
" <td>10797460</td>\n",
" <td>K00752.01</td>\n",
" <td>Kepler-227 b</td>\n",
" <td>CONFIRMED</td>\n",
" <td>CANDIDATE</td>\n",
" <td>1.000</td>\n",
" <td>0</td>\n",
" <td>0</td>\n",
" <td>0</td>\n",
" <td>...</td>\n",
" <td>-81.0</td>\n",
" <td>4.467</td>\n",
" <td>0.064</td>\n",
" <td>-0.096</td>\n",
" <td>0.927</td>\n",
" <td>0.105</td>\n",
" <td>-0.061</td>\n",
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 37
"
"
"
"
<td>291.93423</td>\n",
<td>48.141651</td>\n",
<td>15.347</td>\n",
</tr>\n",
" <tr>\n",
" <th>1</th>\n",
" <td>2</td>\n",
" <td>10797460</td>\n",
" <td>K00752.02</td>\n",
" <td>Kepler-227 c</td>\n",
" <td>CONFIRMED</td>\n",
" <td>CANDIDATE</td>\n",
" <td>0.969</td>\n",
" <td>0</td>\n",
" <td>0</td>\n",
" <td>0</td>\n",
" <td>...</td>\n",
" <td>-81.0</td>\n",
" <td>4.467</td>\n",
" <td>0.064</td>\n",
" <td>-0.096</td>\n",
" <td>0.927</td>\n",
" <td>0.105</td>\n",
" <td>-0.061</td>\n",
" <td>291.93423</td>\n",
" <td>48.141651</td>\n",
" <td>15.347</td>\n",
" </tr>\n",
" <tr>\n",
" <th>2</th>\n",
" <td>3</td>\n",
" <td>10811496</td>\n",
" <td>K00753.01</td>\n",
" <td>NaN</td>\n",
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 38
" <td>FALSE POSITIVE</td>\n",
" <td>FALSE POSITIVE</td>\n",
" <td>0.000</td>\n",
" <td>0</td>\n",
" <td>1</td>\n",
" <td>0</td>\n",
" <td>...</td>\n",
" <td>-176.0</td>\n",
" <td>4.544</td>\n",
" <td>0.044</td>\n",
" <td>-0.176</td>\n",
" <td>0.868</td>\n",
" <td>0.233</td>\n",
" <td>-0.078</td>\n",
" <td>297.00482</td>\n",
" <td>48.134129</td>\n",
" <td>15.436</td>\n",
" </tr>\n",
" <tr>\n",
" <th>3</th>\n",
"source": [
"plt.hist(df[\"koi_prad\"].values, bins=5, color=\"lightblue\")\n",
"plt.title(\"Frequency Distribution for Planet Radius\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 82,
"metadata": {
"id": "YkLOknTVLXvN"
},
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 39
"outputs": [],
"source": [
"df[\"koi_prad\"].fillna(np.nanpercentile(df[\"koi_prad\"].values, 50), inplace = True)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "4ZoJg74VU4Ma"
},
"source": [
"## Replacing NaN in Disposition Score"
]
},
{
"cell_type": "code",
"execution_count": 83,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 299
},
"id": "uSZaRHuHLXo9",
"outputId": "6167771d-c1b5-4a83-e6ca-573a4074674f"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 40
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.scatter(range(df.shape[0]), df[\"koi_score\"].values, label = \"Score\",
color=\"violet\")\n",
"plt.title(\"Disposition Score\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 84,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 354
},
"id": "9XYjIiHXLXi6",
"outputId": "99d5e820-5509-4e9b-b0d8-4c72fd4df337"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
"needs_background": "light"
},
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 41
"output_type": "display_data"
}
],
"source": [
"plt.hist(df[\"koi_score\"].values, color=\"maroon\", bins=6)\n",
"plt.title(\"Frequency Distribution for Disposition Score\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 85,
"metadata": {
"id": "FO-nzcglLXhm"
},
"outputs": [],
"source": [
"df[\"koi_score\"].fillna(np.nanpercentile(df[\"koi_score\"].values, 50), inplace =
True)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "H_07BmzmWD7V"
},
"source": [
"## Replacing NaN in Stellar Surface Gravity"
]
},
{
"cell_type": "code",
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 42
]
},
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.scatter(range(df.shape[0]), df[\"koi_slogg\"].values, label = \"surface gravity\",
color=\"orange\")\n",
"plt.title(\"Stellar Surface Gravity\")\n",
"plt.legend()\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 87,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 354
},
"id": "edss5d_DWDOU",
"outputId": "7998c8b2-809a-458c-d2e0-8e56f4f7d9e6"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 43
},
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.hist(df[\"koi_slogg\"].values, bins=5, color=\"darkviolet\")\n",
"plt.title(\"Frequency Distribution for Stellar Surface Gravity\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 88,
"metadata": {
"id": "qzH8UXJ4WDVX"
},
"outputs": [],
"source": [
"df[\"koi_slogg\"].fillna(np.nanpercentile(df[\"koi_slogg\"].values, 50), inplace =
True)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "smQ4ChxlWcuq"
},
"source": [
"## Replacing NaN in Stellar Radius"
]
},
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 44
{
"cell_type": "code",
"execution_count": 89,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 299
},
"id": "EVGv1-RxWDYY",
"outputId": "30613b82-1131-48f1-f202-7c6c486db258"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.scatter(range(df.shape[0]), df[\"koi_srad\"].values, label = \"Radius\")\n",
"plt.title(\"Stellar Radius\")\n",
"plt.legend()\n",
"plt.grid()"
]
},
{
"cell_type": "code",
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 45
"execution_count": 90,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 354
},
"id": "W4-vTxL8WDdr",
"outputId": "0d7c27f6-1cb3-48e3-c66a-89272942eb9d"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.hist(df[\"koi_srad\"].values, color=\"lightblue\", bins = 5)\n",
"plt.title(\"Frequency Distribution for Stellar Radius\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 91,
"metadata": {
"id": "XSfhLz5tWDbU"
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 46
},
"outputs": [],
"source": [
"df[\"koi_srad\"].fillna(np.nanpercentile(df[\"koi_srad\"].values, 50), inplace = True)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "TL6kAYt-W28Q"
},
"source": [
"## Replacing NaN in Stellar Effective Temperature"
]
},
{
"cell_type": "code",
"execution_count": 92,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 299
},
"id": "BsbZ7rURWDTH",
"outputId": "3345ff32-378f-4b67-d41a-c222ca4fac29"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 47
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.scatter(range(df.shape[0]), df[\"koi_steff\"].values, label = \"temperature\",
color=\"orange\")\n",
"plt.title(\"Stellar Effective Temperature\")\n",
"plt.legend()\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 93,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 354
},
"id": "5rFEdLs7WDRh",
"outputId": "15c903bd-5960-4c75-9d4b-88f4fb75f367"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 48
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.hist(df[\"koi_steff\"].values, color=\"#0504aa\")\n",
"plt.title(\"Frequency Distribution for Stellar Effective Temperature\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 94,
"metadata": {
"id": "BkyIEFs4WDL1"
},
"outputs": [],
"source": [
"df[\"koi_steff\"].fillna(np.nanpercentile(df[\"koi_steff\"].values, 50), inplace = True)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "zALZQafrXSL2"
},
"source": [
"## Replacing NaN in Equilibrium Temperature"
]
},
{
"cell_type": "code",
"execution_count": 95,
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 49
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 299
},
"id": "lTmoh6yqLXaC",
"outputId": "c343b3db-440a-4024-9691-eb00cbd33512"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.scatter(range(df.shape[0]), df[\"koi_teq\"].values, label = \"temperature\",
color=\"darkred\")\n",
"plt.title(\"Equilibrium Temperature\")\n",
"plt.legend()\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 96,
"metadata": {
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 50
"colab": {
"base_uri": "https://localhost:8080/",
"height": 354
},
"id": "mYpZNdmZLXUX",
"outputId": "51a4249e-88ba-448d-86cc-1a53e670bb02"
},
"outputs": [
{
"data": {
"image/png":
"text/plain": [
"<Figure size 432x288 with 1 Axes>"
]
},
"metadata": {
"needs_background": "light"
},
"output_type": "display_data"
}
],
"source": [
"plt.hist(df[\"koi_teq\"].values, color=\"orange\")\n",
"plt.title(\"Frequency Distribution for Equilibrium Temperature\")\n",
"plt.grid()"
]
},
{
"cell_type": "code",
"execution_count": 97,
"metadata": {
"id": "AmkezMGOXeEW"
},
"outputs": [],
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 51
"source": [
"df[\"koi_teq\"].fillna(np.nanpercentile(df[\"koi_teq\"].values, 50), inplace = True)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "-yzHlOt1Xuqo"
},
"source": [
"# Re-Counting NaNs"
]
},
{
"cell_type": "code",
"execution_count": 98,
"metadata": {
"colab": {
"base_uri": "https://localhost:8080/",
"height": 35
},
"id": "fKgQgrho9uuV",
"outputId": "71ed99e2-7536-4c0b-cb39-2da5c516b11b"
},
"outputs": [
{
"name": "stdout",
"output_type": "stream",
"text": [
"{'koi_tce_delivname': 255, 'koi_tce_plnt_num': 255}\n"
]
}
],
"source": [
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 52
"nan_columns = df.isnull().sum()\n",
"nan_columns = {col:count for col, count in nan_columns.items() if count >0}\n",
"pp.pprint(nan_columns)"
]
},
{
"cell_type": "markdown",
"metadata": {
"id": "ORlyVq94ZfwY"
},
"source": [
"# Saving Cleaned Dataset"
]
},
{
"cell_type": "code",
"execution_count": 99,
"metadata": {
"id": "6It_fd4NXs1z"
},
"outputs": [],
"source": [
"#df.to_csv(\"../data/[CLEANED]kepler-data.csv\")"
]
}
],
"metadata": {
"colab": {
"collapsed_sections": [],
"include_colab_link": true,
"name": "Data Cleaning.ipynb",
"provenance": []
},
"kernelspec": {
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 53
"display_name": "Python 3",
"language": "python",
"name": "python3"
},
"language_info": {
"codemirror_mode": {
"name": "ipython",
"version": 3
},
"file_extension": ".py",
"mimetype": "text/x-python",
"name": "python",
"nbconvert_exporter": "python",
"pygments_lexer": "ipython3",
"version": "3.8.3"
}
},
"nbformat": 4,
"nbformat_minor": 1
}
5.3.2 K Means Clustering and Agglomerative Clustering
import numpy as np
import pandas as pd
import matplotlib.cm as cm
import matplotlib.pyplot as plt
import plotly.express as px
from scipy.cluster.hierarchy import dendrogram, linkage
from sklearn.preprocessing import StandardScaler, MinMaxScaler
from sklearn.decomposition import PCA
from sklearn.cluster import KMeans, Birch, AgglomerativeClustering, DBSCAN,
SpectralClustering
from yellowbrick.cluster import KElbowVisualizer, InterclusterDistance,
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 54
SilhouetteVisualizer
getVisualisationPCA(X, y)
model = KMeans(random_state=0)
elbowVisualiser(model)
interclusterDistanceVisualisation(model)
def plot_dendrogram(X):
de = dendrogram(linkage(X, method='ward'))
plt.title('Hierarchical Clustering Dendrogram')
plt.grid()
plt.xlabel("Number of points in node (or index of point if no parenthesis).")
plt.savefig("dendogram.png", dpi=600)
model = AgglomerativeClustering()
elbowVisualiser(model)
plot_dendrogram(X_scaled)
K=7
model = AgglomerativeClustering(n_clusters=K)
viewAggScatter(model)
5.3.3 Support Vector Machine, Random Forest, ADA_Boost
import warnings
warnings.filterwarnings("ignore")
import joblib
import numpy as np
import pandas as pd
import matplotlib.cm as cm
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
from sklearn.svm import SVC
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split, GridSearchCV, KFold,
StratifiedKFold, cross_val_score
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 55
from sklearn.metrics import confusion_matrix, balanced_accuracy_score,
classification_report, cohen_kappa_score, f1_score
from sklearn.ensemble import RandomForestClassifier, AdaBoostClassifier
from yellowbrick.target import FeatureCorrelation
from yellowbrick.features import rank2d, RadViz, Rank2D
from yellowbrick.classifier import DiscriminationThreshold, PrecisionRecallCurve,
ROCAUC
from yellowbrick.model_selection import feature_importances, CVScores, RFECV,
FeatureImportances
from yellowbrick.model_selection import LearningCurve, ValidationCurve
from yellowbrick.classifier import ClassificationReport, ClassPredictionError,
ConfusionMatrix
def getVisualisationPCA(X, y):
x = StandardScaler().fit_transform(X)
pca = PCA(n_components=2)
principal_components = pca.fit_transform(x)
pca_df = pd.DataFrame(
data = principal_components,
columns = ['principal component 1', 'principal component 2']
)
pca_df["TARGET"] = y
labels = np.unique(y)
labels = ["CONFIRMED" if i ==1 else "FALSE POSITIVE" for i in labels]
pca_df["TARGET"] = ["CONFIRMED" if i ==1 else "FALSE POSITIVE" for i in
pca_df["TARGET"].values]
plt.grid()
colors = cm.rainbow(np.linspace(0, 1, len(labels)))
for label, color in zip(labels, colors):
indicesToKeep = pca_df['TARGET'] == label
plt.scatter(
pca_df.loc[indicesToKeep, 'principal component 1'],
pca_df.loc[indicesToKeep, 'principal component 2'],
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 56
c = color,
label=label
)
plt.legend()
plt.grid()
plt.savefig("pca.png", dpi=600)
def getVarianceContribution(X, y):
cols = X.shape[1]
x = StandardScaler().fit_transform(X)
pca = PCA().fit(x)
variance = pca.explained_variance_ratio_
s = np.sum(variance)
p = variance/s
plt.grid()
plt.bar(list(range(1, cols+1)), p)
plt.xlabel('number of components')
plt.ylabel('cumulative explained variance')
plt.savefig("variance.png", dpi=600)
plt.show()
def getFeatureCorrelation(X, y):
visualizer = FeatureCorrelation(labels=TO_USE)
visualizer.fit(X, y)
#visualizer.show("correlation.png", dpi=600)
def getPearsonRanking(X):
#visualizer = rank2d(X, features=TO_USE)
visualizer = Rank2D(algorithm='pearson', features=TO_USE)
visualizer.fit(X, y)
visualizer.transform(X)
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 57
#visualizer.show(outpath="pearson_ranking.png", dpi=600)
def getRadialViz(X, y):
visualizer = RadViz(classes=[0, 1], features = TO_USE)
visualizer.fit(X, y)
visualizer.transform(X)
#visualizer.show("radial.png", dpi=600)
getVisualisationPCA(X, y)
Since the dataset is imbalanced, we cannot use accuracy, hence we opt for the following -
• Confusion Matrix
• F1 Score
• Cohen Kappa Score
• Balanced Accuracy Score
def performance(test, pred):
conf_matrix = confusion_matrix(test, pred)
f1 = f1_score(test, pred)
report = classification_report(test, pred)
accuracy = balanced_accuracy_score(test, pred)
kappa = cohen_kappa_score(test, pred)
print(f"F1 Score: {f1}")
print(f"Kappa Score: {kappa}")
print(f"Accuracy Score: {accuracy}")
print(f"Confusion Matrix:\n{conf_matrix}")
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 58
print(report)
def crossValidationCheck(classifier, X, y, K=10):
cv = KFold(n_splits=K, random_state=1, shuffle=True)
scores = cross_val_score(classifier, X, y, scoring='f1', cv=cv, n_jobs=-1)
print(f"Average F1 score over {K}-Folds: {scores.mean()}")
visualizer = CVScores(classifier, cv=cv, scoring='f1')
visualizer.fit(X, y)
#visualizer.show(f"{str(classifier)[:5]}_cv.png", dpi=600)
visualizer = LearningCurve(classifier, cv=cv, scoring='f1', n_jobs=-1)
visualizer.fit(X, y)
#visualizer.show(f"{str(classifier)[:5]}_learn_curve.png", dpi=600)
cv = StratifiedKFold(n_splits=K, random_state=1, shuffle=True)
scores = cross_val_score(classifier, X, y, scoring='f1', cv=cv, n_jobs=-1)
print(f"Average F1 score over Stratified {K}-Folds: {scores.mean()}")
visualizer = CVScores(classifier, cv=cv, scoring='f1')
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 59
visualizer.fit(X, y)
#visualizer.show(f"{str(classifier)[:5]}_cv_strat.png", dpi=600)
visualizer = LearningCurve(classifier, cv=cv, scoring='f1', n_jobs=-1)
visualizer.fit(X, y)
#visualizer.show(f"{str(classifier)[:5]}_learn_curve_strat.png", dpi=600)
def getFeatureImportance(model, X, y):
viz = FeatureImportances(model, labels=TO_USE)
viz.fit(X, y)
#viz.show(f"{model}_imp.png", dpi=600)
def getClassPredictionError(classifier):
visualizer = ClassPredictionError(classifier, classes=[0, 1])
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_pred_error.png", dpi=600)
def getClassificationReport(classifier):
visualizer = ClassificationReport(classifier, classes=[0, 1])
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 60
#visualizer.show(f"{classifier}_report.png", dpi=600)
def getDiscriminationThreshold(classifier):
visualizer = DiscriminationThreshold(classifier, exclude=["queue_rate"])
visualizer.fit(X, y)
#visualizer.show(f"{classifier}_disc_thresh.png", dpi=600)
def getPrecisionRecall(classifier):
visualizer = PrecisionRecallCurve(classifier)
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_pr.png", dpi=600)
def rocCurve(classifier):
visualizer = ROCAUC(classifier, classes=[0, 1])
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_roc.png", dpi=600)
classifier = SVC(kernel='rbf', random_state=0)
90classifier.fit(X_train, y_train)
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 61
pred = classifier.predict(X_test)
performance(y_test, pred)
F1 Score: 0.9794293297942933
Kappa Score: 0.96934163327601
Accuracy Score: 0.9838579499596449
Confusion Matrix:
[[1521 13]
[ 18 738]]
precision recall f1-score support
0 0.99 0.99 0.99 1534
1 0.98 0.98 0.98 756
accuracy 0.99 2290
macro avg 0.99 0.98 0.98 2290
weighted avg 0.99 0.99 0.99 2290
crossValidationCheck(classifier, X, y, K=10)
classifier = GridSearchCV(
SVC(kernel="rbf", random_state=0),
param_grid=parameters,
scoring=scores,
refit="f1",
verbose=1,
n_jobs=-1
)
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 62
classifier.fit(X_train, y_train)
classifier = RandomForestClassifier(random_state=0, n_jobs=-1)#, max_depth=8,
n_estimators=400, min_samples_leaf=5)
classifier.fit(X_train, y_train)
pred = classifier.predict(X_test)
F1 Score: 0.9839357429718876
Kappa Score: 0.9761603606135845
Accuracy Score: 0.9851332753875126
Confusion Matrix:
[[1531 3]
[ 21 735]]
precision recall f1-score support
0 0.99 1.00 0.99 1534
1 1.00 0.97 0.98 756
accuracy 0.99 2290
macro avg 0.99 0.99 0.99 2290
weighted avg 0.99 0.99 0.99 2290
"""parameters = {
"n_estimators":np.arange(100,700,100),
"max_depth":[None] + np.arange(1, 10, 1).tolist(),
#"min_samples_split":np.arange(0, 1.1, 0.1),
"min_samples_leaf":np.arange(0, 1.1, 0.2),
"max_features":[None ,"sqrt", "log2"], #+ np.arange(1, 1.1, 0.1).tolist(),
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 63
#"min_weight_fraction_leaf":np.arange(0, 11, 1),
#"min_impurity_decrease":np.arange(1, 11, 1),
"class_weight":[None, "balanced", "balanced_subsample"],
#"max_leaf_nodes":[None] + np.arange(1, 11, 1).tolist(),
#"ccp_alpha":np.arange(0, 1.1, 0.1)
}
scores = ["f1", "balanced_accuracy"]"""
classifier = AdaBoostClassifier(random_state=0)
classifier.fit(X_train, y_train)
pred = classifier.predict(X_test)
performance(y_test, pred)
F1 Score: 0.9828042328042328
Kappa Score: 0.9743296565330464
Accuracy Score: 0.9871648282665232
Confusion Matrix:
[[1521 13]
[ 13 743]]
precision recall f1-score support
0 0.99 0.99 0.99 1534
1 0.98 0.98 0.98 756
accuracy 0.99 2290
macro avg 0.99 0.99 0.99 2290
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 64
weighted avg 0.99 0.99 0.99 2290
getClassificationReport(classifier)
getDiscriminationThreshold(classifier)
getPrecisionRecall(classifier)
rocCurve(classifier)
crossValidationCheck(classifier, X, y, K=10)
Average F1 score over 10-Folds: 0.9793646173099949
Average F1 score over Stratified 10-Folds: 0.9798501667467722
parameters = {
"n_estimators":np.arange(70,130,10),
"learning_rate":np.arange(0.8,1.2,0.05),
"algorithm":["SAMME", "SAMME.R"],
"base_estimator":[
DecisionTreeClassifier(max_depth=1),
DecisionTreeClassifier(max_depth=2),
DecisionTreeClassifier(max_depth=3),
DecisionTreeClassifier(max_depth=None)
]
}
scores = ["f1", "balanced_accuracy"]
classifier = GridSearchCV(
AdaBoostClassifier(random_state=0),
param_grid=parameters,
scoring=scores,
refit="f1",
verbose=1,
n_jobs=-1
)
classifier.fit(X_train, y_train)
F1 Score: 0.9814323607427056
Kappa Score: 0.9723178730179562
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 65
Accuracy Score: 0.9855066465235957
Confusion Matrix:
[[1522 12]
[ 16 740]]
precision recall f1-score support
0 0.99 0.99 0.99 1534
1 0.98 0.98 0.98 756
accuracy 0.99 2290
macro avg 0.99 0.99 0.99 2290
weighted avg 0.99 0.99 0.99 2290
Error:
import warnings
warnings.filterwarnings("ignore")
import joblib
import numpy as np
import pandas as pd
import matplotlib.cm as cm
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
from sklearn.svm import SVC
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split, GridSearchCV, KFold, StratifiedKFold,
cross_val_score
from sklearn.metrics import confusion_matrix, balanced_accuracy_score, classification_repor
t, cohen_kappa_score, f1_score
from sklearn.ensemble import RandomForestClassifier, AdaBoostClassifier
from yellowbrick.target import FeatureCorrelation
from yellowbrick.features import rank2d, RadViz, Rank2D
from yellowbrick.classifier import DiscriminationThreshold, PrecisionRecallCurve, ROCAU
C
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 66
from yellowbrick.model_selection import feature_importances, CVScores, RFECV, FeatureI
mportances
from yellowbrick.model_selection import LearningCurve, ValidationCurve
from yellowbrick.classifier import ClassificationReport, ClassPredictionError, ConfusionMat
rix
df = pd.read_csv("../data/[CLEANED]kepler-data.csv")
df.drop(columns = ["Unnamed: 0"], inplace=True)
print(df.shape)
df.head()
Selecting Columns for Prediction¶
We eliminate all the columns that are either of the following
• Assigned after other values are measured from readings
• Contain ID or name attributes
• Are error attributes
ALL_COLUMNS = df.columns
ERROR_COLUMNS = [col for col in ALL_COLUMNS if "err" in col]
EXCLUDE = ["rowid", "kepid", "kepoi_name", "koi_score", "koi_disposition",
"koi_pdisposition", "koi_tce_delivname", "koi_tce_plnt_num"]# + ERROR_COLUMNS
TO_USE = list(set(ALL_COLUMNS) - set(EXCLUDE))
print(f"Columns being analysed: {len(TO_USE)}")
df[TO_USE].head()
def getVisualisationPCA(X, y):
x = StandardScaler().fit_transform(X)
pca = PCA(n_components=2)
principal_components = pca.fit_transform(x)
pca_df = pd.DataFrame(
data = principal_components,
columns = ['principal component 1', 'principal component 2']
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 67
)
pca_df["TARGET"] = y
labels = np.unique(y)
labels = ["CONFIRMED" if i ==1 else "FALSE POSITIVE" for i in labels]
pca_df["TARGET"] = ["CONFIRMED" if i ==1 else "FALSE POSITIVE" for i in
pca_df["TARGET"].values]
plt.grid()
colors = cm.rainbow(np.linspace(0, 1, len(labels)))
for label, color in zip(labels, colors):
indicesToKeep = pca_df['TARGET'] == label
plt.scatter(
pca_df.loc[indicesToKeep, 'principal component 1'],
pca_df.loc[indicesToKeep, 'principal component 2'],
c = color,
label=label
)
plt.legend()
plt.grid()
plt.savefig("pca_error.png", )
plt.show()
def getVarianceContribution(X, y):
cols = X.shape[1]
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 68
x = StandardScaler().fit_transform(X)
pca = PCA().fit(x)
variance = pca.explained_variance_ratio_
s = np.sum(variance)
p = variance/s
#print(variance)
plt.grid()
plt.bar(list(range(1, cols+1)), p)
plt.xlabel('number of components')
plt.ylabel('cumulative explained variance')
plt.grid()
plt.savefig("variance_error.png", dpi=600)
plt.show()
def getFeatureCorrelation(X, y):
visualizer = FeatureCorrelation(labels=TO_USE)
visualizer.fit(X, y)
visualizer.show("correlation_error.png", dpi=600)
def getPearsonRanking(X):
visualizer = Rank2D(algorithm='pearson', features=TO_USE)
visualizer.fit(X, y)
visualizer.transform(X)
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 69
#visualizer.show()
visualizer.show(outpath="pearson_ranking_error.png", dpi=600)
def getRadialViz(X, y):
visualizer = RadViz(classes=[0, 1], features = TO_USE)
visualizer.fit(X, y)
visualizer.transform(X)
visualizer.show("radial_error.png", dpi=600)
We need to hence using different techniques of non-linear classification, which can handle
the non-linearity issue as well as class imbalance. We can employ Bagging or Boosting
Techniques such as
• SVM
• Random Forests
• AdaBoost
def getFeatureImportance(model, X, y):
viz = FeatureImportances(model, labels=TO_USE)
viz.fit(X, y)
#viz.show(f"{model}_imp_error.png", dpi=600)
def getClassPredictionError(classifier):
visualizer = ClassPredictionError(classifier, classes=[0, 1])
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_pred_error_error.png", dpi=600)
def getClassificationReport(classifier):
visualizer = ClassificationReport(classifier, classes=[0, 1])
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 70
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_report_error.png", dpi=600)
def getDiscriminationThreshold(classifier):
visualizer = DiscriminationThreshold(classifier, exclude=["queue_rate"])
visualizer.fit(X, y)
#visualizer.show(f"{classifier}_disc_thresh_error.png", dpi=600)
def getPrecisionRecall(classifier):
visualizer = PrecisionRecallCurve(classifier)
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_pr_error.png", dpi=600)
def rocCurve(classifier):
visualizer = ROCAUC(classifier, classes=[0, 1])
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
#visualizer.show(f"{classifier}_roc_error.png", dpi=600)
classifier = SVC(kernel='rbf', random_state=0)
classifier.fit(X_train, y_train)
pred = classifier.predict(X_test)
F1 Score: 0.9846564376250834
Kappa Score: 0.977192163492392
Accuracy Score: 0.9864655118892407
Confusion Matrix:
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 71
[[1529 5]
[ 18 738]]
precision recall f1-score support
0 0.99 1.00 0.99 1534
1 0.99 0.98 0.98 756
accuracy 0.99 2290
macro avg 0.99 0.99 0.99 2290
weighted avg 0.99 0.99 0.99 2290
crossValidationCheck(classifier, X, y, K=10)
def crossValidationCheck(classifier, X, y, K=10):
cv = KFold(n_splits=K, random_state=1, shuffle=True)
scores = cross_val_score(classifier, X, y, scoring='f1', cv=cv, n_jobs=-1)
print(f"Average F1 score over {K}-Folds: {scores.mean()}")
visualizer = CVScores(classifier, cv=cv, scoring='f1')
visualizer.fit(X, y)
#visualizer.show(f"{classifier[:5]}_cv_error.png", dpi=600)
visualizer = LearningCurve(classifier, cv=cv, scoring='f1', n_jobs=-1)
visualizer.fit(X, y)
#visualizer.show(f"{classifier[:5]}_learn_curve_error.png", dpi=600)
cv = StratifiedKFold(n_splits=K, random_state=1, shuffle=True)
scores = cross_val_score(classifier, X, y, scoring='f1', cv=cv, n_jobs=-1)
print(f"Average F1 score over Stratified {K}-Folds: {scores.mean()}")
visualizer = CVScores(classifier, cv=cv, scoring='f1')
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 72
visualizer.fit(X, y)
#visualizer.show(f"{classifier[:5]}_cv_strat_error.png", dpi=600)
visualizer = LearningCurve(classifier, cv=cv, scoring='f1', n_jobs=-1)
visualizer.fit(X, y)
#visualizer.show(f"{classifier[:5]}_learn_curve_strat_error.png", dpi=600)
classifier = RandomForestClassifier(random_state=0, n_jobs=-1)#, max_depth=8,
n_estimators=400, min_samples_leaf=5)
classifier.fit(X_train, y_train)
pred = classifier.predict(X_test)
F1 Score: 0.9757085020242915
Kappa Score: 0.9640951400394066
Accuracy Score: 0.9771967674510047
Confusion Matrix:
[[1531 3]
[ 33 723]]
precision recall f1-score support
0 0.98 1.00 0.99 1534
1 1.00 0.96 0.98 756
accuracy 0.98 2290
macro avg 0.99 0.98 0.98 2290
weighted avg 0.98 0.98 0.98 2290
getClassificationReport(classifier)
getDiscriminationThreshold(classifier)
classifier = GridSearchCV(
SVC(kernel="rbf", random_state=0),
param_grid=parameters,
scoring=scores,
refit="f1",
verbose=1,
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 73
n_jobs=-1
)
[Parallel(n_jobs=-1)]: Using backend LokyBackend with 8 concurrent workers.
[Parallel(n_jobs=-1)]: Done 34 tasks | elapsed: 0.9s
[Parallel(n_jobs=-1)]: Done 320 tasks | elapsed: 8.7s
[Parallel(n_jobs=-1)]: Done 820 tasks | elapsed: 20.2s
[Parallel(n_jobs=-1)]: Done 1520 tasks | elapsed: 36.1s
[Parallel(n_jobs=-1)]: Done 2420 tasks | elapsed: 57.2s
[Parallel(n_jobs=-1)]: Done 3520 tasks | elapsed: 1.4min
[Parallel(n_jobs=-1)]: Done 4820 tasks | elapsed: 1.8min
[Parallel(n_jobs=-1)]: Done 6320 tasks | elapsed: 2.4min
[Parallel(n_jobs=-1)]: Done 8020 tasks | elapsed: 3.0min
[Parallel(n_jobs=-1)]: Done 9920 tasks | elapsed: 3.6min
[Parallel(n_jobs=-1)]: Done 12020 tasks | elapsed: 4.4min
[Parallel(n_jobs=-1)]: Done 14320 tasks | elapsed: 5.1min
[Parallel(n_jobs=-1)]: Done 16820 tasks | elapsed: 6.0min
[Parallel(n_jobs=-1)]: Done 19520 tasks | elapsed: 6.9min
[Parallel(n_jobs=-1)]: Done 22420 tasks | elapsed: 7.8min
[Parallel(n_jobs=-1)]: Done 22665 out of 22680 | elapsed: 7.9min remaining: 0.2s
[Parallel(n_jobs=-1)]: Done 22680 out of 22680 | elapsed: 7.9min finished
classifier.fit(X_train, y_train)
getPrecisionRecall(classifier)
crossValidationCheck(classifier, X, y, K=10)
"""parameters = {
"n_estimators":np.arange(100,700,100),
"max_depth":[None] + np.arange(1, 10, 1).tolist(),
#"min_samples_split":np.arange(0, 1.1, 0.1),
"min_samples_leaf":np.arange(0, 1.1, 0.2),
"max_features":[None ,"sqrt", "log2"], #+ np.arange(1, 1.1, 0.1).tolist(),
#"min_weight_fraction_leaf":np.arange(0, 11, 1),
#"min_impurity_decrease":np.arange(1, 11, 1),
"class_weight":[None, "balanced", "balanced_subsample"],
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 74
#"max_leaf_nodes":[None] + np.arange(1, 11, 1).tolist(),
#"ccp_alpha":np.arange(0, 1.1, 0.1)
}
scores = ["f1", "balanced_accuracy"]"""
classifier = AdaBoostClassifier(random_state=0)
classifier.fit(X_train, y_train)
red = classifier.predict(X_test)
performance(y_test, pred)
F1 Score: 0.9692101740294512
Kappa Score: 0.9543073578427035
Accuracy Score: 0.9742727454591862
Confusion Matrix:
[[1520 14]
[ 32 724]]
precision recall f1-score support
0 0.98 0.99 0.99 1534
1 0.98 0.96 0.97 756
accuracy 0.98 2290
macro avg 0.98 0.97 0.98 2290
weighted avg 0.98 0.98 0.98 2290
getClassificationReport(classifier)
getDiscriminationThreshold(classifier)
crossValidationCheck(classifier, X, y, K=10)
Average F1 score over 10-Folds: 0.962738683786076
Average F1 score over Stratified 10-Folds: 0.966524885983963
parameters = {
"n_estimators":np.arange(50,150,10),
"learning_rate":np.arange(0.5,1.5,0.05),
"algorithm":["SAMME", "SAMME.R"],
"base_estimator":[
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 75
DecisionTreeClassifier(max_depth=1),
DecisionTreeClassifier(max_depth=2),
DecisionTreeClassifier(max_depth=3),
DecisionTreeClassifier(max_depth=None)
]
}
scores = ["f1", "balanced_accuracy"]
classifier = GridSearchCV(
AdaBoostClassifier(random_state=0),
param_grid=parameters,
scoring=scores,
refit="f1",
verbose=1,
n_jobs=-1
)
classifier.fit(X_train, y_train)
classifier = GridSearchCV(
AdaBoostClassifier(random_state=0),
param_grid=parameters,
scoring=scores,
refit="f1",
verbose=1,
n_jobs=-1
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 76
)
classifier.fit(X_train, y_train)
F1 Score: 0.9819639278557114
Kappa Score: 0.9732075304908963
Accuracy Score: 0.9841554396639143
Confusion Matrix:
[[1528 6]
[ 21 735]]
precision recall f1-score support
0 0.99 1.00 0.99 1534
1 0.99 0.97 0.98 756
accuracy 0.99 2290
macro avg 0.99 0.98 0.99 2290
weighted avg 0.99 0.99 0.99 2290
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 77
CHAPTER 6
CONCLUSION
The inspection gives the finishing touch and confer supreme valuable judgments about this
inquest. The tactics that are accommodated here are mainly used to line up the exoplanets. This
is gained by a well thought out plan and virtuous team work. To attain this goal, the comprising
machine leaning techniques are used. The bearing deployment of machine learning models
exhibit the perfection of data science projects. So, by using the machine learning models time
consumption is reduced to its maximum with a perfect information that is needed. The objective
is to get the profound data of the planetary objects to discover the aspects that will let the life
comfort on those planetary objects. Also, to discover many research papers for the future
purposes. The machine learning models discussed are very helpful to get the accurate results.
Finally, this planned effort made in this study and the results from this study can be verifiable
again when needed. The immense level of qualified domain will be able to achieve the innards
of this study. Also, the previous research papers are helpful for the future scientific efforts and
discoveries. In the forthcoming studies, the astrophysics will play the prominent role in
resolving the problems that is currently being experienced by the planets. The reliable survey
of this exoplanets and their evolution is generously helpful to undo the aspects that is useful to
find the life comfort which is our main aim.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 78
 FUTURE ENANCEMENTS
We now return to the tasks posed to develop the technology to detect the full range of exoplanet masses 
and orbital parameters, and to understand the formation, dynamics, and physical properties of the planets 
that are already known. The bearing deployment of machine learning models exhibit the perfection of 
data science projects. So, by using the machine learning models time consumption is reduced to its 
maximum with a perfect information that is needed. The objective is to get the profound data of the 
planetary objects to discover the aspects that will let the life comfort on those planetary objects. These 
tasks can be re-stated more specifically as detecting an Earth-mass planet in the habitable zone of a solartype star and probing its atmosphere for signs of life. This latter task requires spectroscopy, and hence 
the planet must either transit or be accessible to direct imaging. Given the current limitations of groundbased adaptive optics, it is possible that Earth-analogues will first be detected with space-based 
telescopes. Detecting and probing the atmosphere of an Earth-analogue by any of the above methods will 
require greater coordination and consensus amongst the exoplanet research community than any other 
task in the field’s short, eventful history. As the first cohort of astronomers with the tools to realize these 
goals, we have much to look forward to.
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 79
REFERENCES
[1] Habitability of Exoplanets using Deep learning. - 14 May 2021
Toronto, ON, Canada Rutuja Jagtap; Unzela Inamdar; Shivani Dere
(IEEE)
[2] Machine Learning Pipeline for Exoplanet Classification, Vol. 2: No. 1,
Article 9 – 2019 Brychan Manry; George Sturrock; Sohaila Rafiqi;
(SMU Data Science Review)
[3] Predicting habitable exoplanets from NASA's Kepler mission data
using Machine Learning - 2017; Rajeev Mishra; (Stanford University)
[4] Classifying Exoplanets as Potentially Habitable Using Machine
Learning – 2018 Karan Hora; (Cornell University)
[5] Identifying Exoplanets with Deep Learning: A Five-planet Resonant
Chain around Kepler-80 and an Eighth Planet around Kepler-90 - 2018
Christopher J; Shallue1; Andrew Vanderburg;
[6] Finding New Earths Using Machine Learning & Committee Machine -
2020 Piyush Gawade; Akshay Mayekar; Ashish Bhosale; Dr. Sanjay
Jadhav; (IRJE)
[7] Exoplanet Hunting in Deep Space with Machine Learning - 2020
Shivam Pratap Singh; Devendra Kumar Misra; (IJRESM)
[8] Transiting Exoplanet Discovery Using Machine Learning Techniques
- 2020 Miguel Jara-Maldonado et.al (Earth Informatics and Science)
[9] Machine-learning-based pipeline to identify and evaluate planet
candidates from TESS -27 January 2021, California USA Sriram Rao;
ANALYSIS AND EVALUATION OF HABITABLE EXOPLANETS RESEMBLANT TO TERRA
Dept Of CSE, ACSCE 2021-22 80
Ashish Mahabal (IEEE)
[10] Habitability Classification of Exoplanets: A Machine Learning Insight.
- 21 July 2021 Pennsylvania state university Suryoday Basak; Archana
Mathur; Jayanth Murthy (European Journal)
[11] Searching for Exoplanets using Artificial Intelligence - 07 May 2018
Planetary Laboratory University of Arizona. Kyle A. Pearson, Leon
Palafox, and Caitlin A. Griffith (University of Arizona)
Websites:
[11] https://exoplanetarchive.ipac.caltech.edu/
[12] https://www.coursera.org/learn/machine-learning
[13] https://data.nasa.gov/dataset/Kepler/crwh-g7rq
[14] https://stackoverflow.com/questions/tagged/machine-learning
[15] https://www.geeksforgeeks.org/machine-learning
