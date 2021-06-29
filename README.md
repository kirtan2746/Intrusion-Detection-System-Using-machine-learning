# Intrusion-Detection-System-Using-machine-learning

# INTRODUCTION

Every day millions of people and hundreds of thousands of institutions communicate with each 
other over the Internet. In the past two decades, while the number of people using the Internet has 
increased very fast, today this number has exceeded 4 billion and this increase is continuing 
rapidly.

# IDS OVERVIEW

An Intrusion Detection System (IDS) is a system that monitors network traffic for suspicious 
activity and issues alerts when such activity is discovered. It is a software application that scans a 
network or a system for harmful activity or policy breaching. Any malicious venture or violation 
is normally reported either to an administrator or collected centrally using a security information 
and event management (SIEM) system. A SIEM system integrates outputs from multiple sources 
and uses alarm filtering techniques to differentiate malicious activity from false alarms.
Although intrusion detection systems monitor networks for potentially malicious activity, they are 
also disposed to false alarms. Hence, organizations need to fine-tune their IDS products when they 
first install them. It means properly setting up the intrusion detection systems to recognize what 
normal traffic on the network looks like as compared to malicious activity.
Intrusion prevention systems also monitor network packets inbound the system to check the 
malicious activities involved in it and at once sends the warning notifications

# Classification of Intrusion Detection System:

1. Network Intrusion Detection System (NIDS) :
Network intrusion detection systems (NIDS) are set up at a planned point within the network 
to examine traffic from all devices on the network. It performs an observation of passing traffic 
on the entire subnet and matches the traffic that is passed on the subnets to the collection of 
known attacks. Once an attack is identified or abnormal behaviour is observed, the alert can be 
sent to the administrator. An example of an NIDS is installing it on the subnet where firewalls 
are located in order to see if someone is trying crack the firewall.

2. Host Intrusion Detection System (HIDS) :
Host intrusion detection systems (HIDS) run on independent hosts or devices on the network. 
A HIDS monitors the incoming and outgoing packets from the device only and will alert the 
administrator if suspicious or malicious activity is detected. It takes a snapshot of existing 
system files and compares it with the previous snapshot. If the analytical system files were 
edited or deleted, an alert is sent to the administrator to investigate. An example of HIDS usage 
can be seen on mission critical machines, which are not expected to change their layout.

# DATASETS
# 1) KDD’99 
Since 1999, KDD’99 has been the most wildly used data set for the evaluation of anomaly 
detection methods. This data set is prepared by Stolfo et al. and is built based on the data captured 
in DARPA’98 IDS evaluation program. DARPA’98 is about 4 gigabytes of compressed raw 
(binary) tcp dump data of 7 weeks of network traffic, which can be processed into about 5 million 
connection records, each with about 100 bytes. The two weeks of test data have around 2 million 
connection records. KDD training dataset consists of approximately 4,900,000 single connection 
vectors each of which contains 41 features and is labelled as either normal or an attack, with exactly 
one specific attack type. The simulated attacks fall in one of the following four categories:
1) Denial of Service Attack (DoS): is an attack in which the attacker makes some computing or 
memory resource too busy or too full to handle legitimate requests, or denies legitimate users 
access to a machine. 
2) User to Root Attack (U2R): is a class of exploit in which the attacker starts out with access to 
a normal user account on the system (perhaps gained by sniffing passwords, a dictionary attack, 
or social engineering) and is able to exploit some vulnerability to gain root access to the system. 
3) Remote to Local Attack (R2L): occurs when an attacker who has the ability to send packets 
to a machine over a network but who does not have an account on that machine exploits some 
vulnerability to gain local access as a user of that machine. 
4) Probing Attack: is an attempt to gather information about a network of computers for the 
apparent purpose of circumventing its security controls. 
It is important to note that the test data is not from the same probability distribution as the training 
data, and it includes specific attack types not in the training data which make the task more 
realistic. Some intrusion experts believe that most novel attacks are variants of known attacks and 
the signature of known attacks can be sufficient to catch novel variants. 
The datasets contain a total number of 24 training attack types, with an additional 14 types in the 
test data only. The name and detail description of the training attack types are listed in. 

# 2) CICIDS2017
The CICIDS 2017 (Intrusion Detection Evaluation Dataset) created by the Canadian Institute for 
Cybersecurity at the University of New Brunswick. This dataset consists of a 5-day (3rd July- 7th 
July 2017) data stream on a network created by computers using up-to-date operating systems such 
as Windows Vista / 7 / 8.1 / 10, Mac, Ubuntu 12/16 and Kali.

The CICIDS 2017 data set has the following advantages over the other datasets mentioned 
above: 

• The obtained data is the real-world data; was obtained from a testbed consisting of real 
computers. 
• Data streams are collected from computers with the up-to-date operating system. There is 
operating system diversity (Mac, Windows, and Linux) between both attacker and victim 
computers. 
• Data sets are labelled. In order to apply the machine learning methods, the feature extraction, 
which is a critical step, was applied and 85 features (see Appendix A for the feature list) were 
obtained. 
• Both raw data (pcap files - captured network packets files) and processed data (CSV filescomma-separated data files) are available to work on. 

# Methodology
# Tools and Methods 

Software Platform 

Python, a free and open-source object-oriented programming language, draws 
attention with its simple syntax and dynamic structure. In Python, it's very easy to 
write code and analyse code. Another advantage is that it has the advantage of 
extensive documentation (books, internet sites, forums, etc.). In addition to all these 
advantages, it works in concert with many libraries which "machine learning" 
applications can be done. In this context, Python3.7 has been chosen to be used in 
this work, because of many of the advantages it provides. 

Sklearn (Scikit-learn) is a machine learning library that can be used with the Python 
programming language. Sklearn offers a wide range of options to the user with its 
numerous machine learning algorithms. Sklearn has extensive documentation and 
contains all the algorithms needed for this work. 

Pandas is a powerful data analysis library running on Python. When working with 
a large dataset, Pandas allows you to easily perform many operations such as 
filtering, bulk column / row deletion, addition, and replacement. Because of all these 
advantages, the Pandas library has been used. 

Matplotlib is a library that runs on Python, allowing visualization of data. This 
library is used to create graphs used in the study

NumPy, a Python library that allows you to perform mathematical and logical 
operations quickly and easily, has been used in calculations in this work. 

Hardware Platform 
An evaluation criterion for machine learning algorithms is the execution time. 
However, the execution time may vary depending on the performance of the 
computer being used. Because of this, the technical specifications of the computer 
used in the application are shared. The technical characteristics of the computer used 
in the implementation phase are


# DATA Pre-processing

1) Pre-processing of KDD

❖ First let’s analyse kdd’99 dataset, here is first few entries of kdd’99 dataset
❖ After that we will remove all null rows 
❖ Now we have to find possible co-relation between dataset 
❖ To find all possible co-relation I used heat-map to represent data in graphical 
manne

2) Pre-processing of CICIDS2017


It may be necessary to make some changes to the dataset before using it in practice, 
making it more efficient. For this purpose, in this section, some defects of the 
CICIDS2017 dataset are corrected, and some data are edited.

The dataset file contains 3119345 stream records. The distribution of these stream 
records can be seen from Table 2. When these records are examined, it can be seen 
that the 288602 record is incorrect / incomplete3. The first step in the pre-processing 
process will be to delete these unnecessary records.

Another error about the dataset is in the columns that make up the features. The 
dataset file consists of 86 columns that define the flow properties such as Flow ID, 
Source IP, Source Port etc. However, the Fwd Header Length feature (which defines 
the forward direction data flow for total bytes used) was written two times (41st and 
62nd columns). This error is corrected by deleting the repeating column .

Another change that needs to be made in the dataset is to convert the properties 
including the categorical and string values (Flow ID, Source IP, Destination IP, 
Timestamp, External IP) into numerical data to be used in machine learning 
algorithms. This can be done with LabelEncoder() from Sklearn classes. In this way, 
various string values that cannot be used in machine learning operations will get 
integer values between 0 and n-1 and will become more suitable for processing.

# 1) KNN
K-nearest neighbors (KNN) algorithm uses ‘feature similarity’ to predict the values of new 
datapoints which further means that the new data point will be assigned a value based on how 
closely it matches the points in the training set. We can understand its working with the help of 
following steps −
Step 1 − For implementing any algorithm, we need dataset. So during the first step of KNN, we 
must load the training as well as test data.
Step 2 − Next, we need to choose the value of K i.e. the nearest data points. K can be any integer.
Step 3 − For each point in the test data do the following −
❖ 3.1 − Calculate the distance between test data and each row of training data with the help 
of any of the method namely: Euclidean, Manhattan or Hamming distance. The most 
commonly used method to calculate distance is Euclidean.
❖ 3.2 − Now, based on the distance value, sort them in ascending order.
❖ 3.3 − Next, it will choose the top K rows from the sorted array.
❖ 3.4 − Now, it will assign a class to the test point based on most frequent class of these rows.
❖ Step 4 − End

# 2) Decision tree

In general, Decision tree analysis is a predictive modelling tool that can be applied across many 
areas. Decision trees can be constructed by an algorithmic approach that can split the dataset in 
different ways based on different conditions. Decisions tress are the most powerful algorithms that 
falls under the category of supervised algorithms.

They can be used for both classification and regression tasks. The two main entities of a tree are 
decision nodes, where the data is split and leaves, where we got outcome. The example of a binary 
tree for predicting whether a person is fit or unfit providing various information like age, eating 
habits and exercise habits.

2) Decision tree
In general, Decision tree analysis is a predictive modelling tool that can be applied across many 
areas. Decision trees can be constructed by an algorithmic approach that can split the dataset in 
different ways based on different conditions. Decisions tress are the most powerful algorithms that 
falls under the category of supervised algorithms.
They can be used for both classification and regression tasks. The two main entities of a tree are 
decision nodes, where the data is split and leaves, where we got outcome. The example of a binary 
tree for predicting whether a person is fit or unfit providing various information like age, eating 
habits and exercise habits, is given below

2) Decision tree
In general, Decision tree analysis is a predictive modelling tool that can be applied across many 
areas. Decision trees can be constructed by an algorithmic approach that can split the dataset in 
different ways based on different conditions. Decisions tress are the most powerful algorithms that 
falls under the category of supervised algorithms.
They can be used for both classification and regression tasks. The two main entities of a tree are 
decision nodes, where the data is split and leaves, where we got outcome. The example of a binary 
tree for predicting whether a person is fit or unfit providing various information like age, eating 
habits and exercise habits, is given below

# 3) Support Vector Machine(SVM)

Support Vector Machines or SVM in-short, is one of the most popular and talked about
algorithms, and were extremely popular around the time they were developed and refined in
the 1990s, and continued to be popular and is one of the best choices for high-performance
algorithms with a little tuning and it presents one of the most robust prediction methods.

SVM is implemented uniquely when compared to other ML algorithms. An SVM training
algorithm builds a model that assigns new examples to one category or the other, making it a
non-probabilistic binary linear classifier.

SVM is a Supervised Learning algorithm, which is used for Classification as well as Regression
problems. However, primarily, it is used for Classification problems in Machine Learning. In
addition to performing linear classification, SVMs can efficiently perform a non-linear
classification as well using a trick or parameter called as Kernel, which implicitly maps their
inputs into high-dimensional feature spaces.Will see the details about the Kernel soon.

SVM is also an Unsupervised Learning algorithm. When data is unlabelled, supervised learning
is not possible, and an unsupervised learning approach is required, which attempts to find
natural clustering of the data to groups, and then map new data to these formed groups.
The support-vector clustering algorithm, created by Hava Siegelmann and Vladimir Vapnik,
applies the statistics of support vectors, developed in the support vector machines algorithm,
to categorize unlabeled data, and is one of the most widely used clustering algorithms in
industrial applications.

Definition of SVM

A support Vector Machine is a discriminative classifier formally defined by a separating
hyperplane. In other words, given labelled training data (supervised learning), the algorithm
outputs an optimal hyperplane which categorizes new examples. In two dimensional space, this
hyperplane is a line dividing a plane into two parts wherein each class lay in either side.

In simple terms, I could explain SVM as a model that represents the data points in space,
mapped such that the data points of the separate categories are divided by a clear gap that is as
wide as possible.

For 1 Dimensional data, the support vector classifier is a point. Similarly, for 2 Dimensional
data, the support vector classifier will be a line, and for 3-dimensional data, a support vector
classifier is a plane. And for 4 dimensional or more, the support vector classifier will be a
hyperplane.

Implementation

We have two choices, we can either use the sci-kit learn library to import the SVM model and
use it directly or we can write our model from scratch.
It's really fun and interesting creating the model from scratch, but that requires a lot of patience
and time.

Instead, using a library from sklearn.SVM module which includes Support Vector Machine
algorithms will be much easier in implementation as well as to tune the parameters.
Will be writing another article dedicated to the hand-on with the SVM algorithms including
classification and regression problems and we shall tweak and play tuning parameters. Also
will do a comparison on Kernel performance.

SVM Use Cases

Some use-cases of SVM are as below.

 Face Detection
 Bioinformatics
 Classification of Images
 Remote Homology Detection
 Handwriting Detection
 Generalized Predictive Control
 Text and Hypertext Categorization
 Intrusion detection system

# 4) Artificial Neural Network (ANN)

The term "Artificial neural network" refers to a biologically inspired sub-
field of artificial intelligence modeled after the brain. An Artificial neural network is usually a

computational network based on biological neural networks that construct the structure of the
human brain. Similar to a human brain has neurons interconnected to each other, artificial
neural networks also have neurons that are linked to each other in various layers of the
networks. These neurons are known as nodes.

Artificial neural network tutorial covers all the aspects related to the artificial neural network.
In this tutorial, we will discuss ANNs, Adaptive resonance theory, Kohonen self-organizing
map, Building blocks, unsupervised learning, Genetic algorithm, etc.

What is Artificial Neural Network?The term "Artificial Neural Network" is derived from
Biological neural networks that develop the structure of a human brain. Similar to the human
brain that has neurons interconnected to one another, artificial neural networks also have
neurons that are interconnected to one another in various layers of the networks. These neurons
are known as nodes.

An Artificial Neural Network in the field of Artificial intelligence where it attempts to mimic
the network of neurons makes up a human brain so that computers will have an option to
understand things and make decisions in a human-like manner. The artificial neural network is
designed by programming computers to behave simply like interconnected brain cells.
There are around 1000 billion neurons in the human brain. Each neuron has an association
point somewhere in the range of 1,000 and 100,000. In the human brain, data is stored in such
a manner as to be distributed, and we can extract more than one piece of this data when
necessary from our memory parallelly. We can say that the human brain is made up of
incredibly amazing parallel processors.

We can understand the artificial neural network with an example, consider an example of a
digital logic gate that takes an input and gives an output. "OR" gate, which takes two inputs. If
one or both the inputs are "On," then we get "On" in output. If both the inputs are "Off," then
we get "Off" in output. Here the output depends upon input. Our brain does not perform the
same task. The outputs to inputs relationship keep changing because of the neurons in our brain,
which are "learning."

Types of Artificial Neural Network: 

There are various types of Artificial Neural Networks

(ANN) depending upon the human brain neuron and network functions, an artificial neural
network similarly performs tasks. The majority of the artificial neural networks will have some
similarities with a more complex biological partner and are very effective at their expected
tasks. For example, segmentation or classification.


Feedback ANN: In this type of ANN, the output returns into the network to accomplish the
best-evolved results internally. As per the University of Massachusetts, Lowell Centre for
Atmospheric Research. The feedback networks feed information back into itself and are well
suited to solve optimization issues.


Feed-Forward ANN: A feed-forward network is a basic neural network comprising of an input
layer, an output layer, and at least one layer of a neuron. Through assessment of its output by
reviewing its input, the intensity of the network can be noticed based on group behavior of the
associated neurons, and the output is decided.

# Performance Evaluation Methods

The results of this study are evaluated according to four criteria, namely accuracy, precision,
f-measure, and recall. All these criteria take a value between 0 and 1. When it approaches 1,
the performance increases, while when it approaches 0, it decreases.

Accuracy: The ratio of successfully categorized data to total data .

Accuracy = TN+TP/FP+TN+TP+FN

Recall (Sensitivity): The ratio of data classified as an attack to all attack data.
Recall = TP/TP+FN

Precision: The ratio of successful classified data as the attack to all data classified as the attack
Precision = TP/FP+TP

F-measure (F-score/F1-score): The harmonic-mean of sensitivity and precision. This concept
is used to express the overall success. so, in this study, when analysing the results, it will be
focused, especially on the F1 Score.
F- measure = 2 1 Recall + 1 Precision

In calculating these four items, the four values summarized below are used:

• TP: True Positive (Correct Detection) The attack data classified as attack
• FP: False Positive (Type-1 Error) The benign data classified as attack.
• FN: False Negative (Type-2 Error) The attack data classified as benign.
• TN: True Negative (Correct Rejection) The benign data classified as benign.

# Results



Algorithm KDD’99 And CICIDS2017

SVM ON KDD :-  99.87
SVM ON CICIDS :-  94.97

ANN ON KDD :-  99.74
ANN ON CICIDS :- 97.95

KNN ON KDD:-  80.88
KNN ON CICIDS :- 86.12

DT ON KDD :-  89.67 
DT ON CICIDS :- 96.00

# Deployment

HTML

HTML (Hypertext Mark-up Language) is the code that is used to structure a web page and its
content. For example, content could be structured within a set of paragraphs, a list of bulleted
points, or using images and data tables.

Web browsers receive HTML documents from a web server or from local storage and render
the documents into multimedia web pages. HTML describes the structure of a web page
semantically and originally included cues for the appearance of the document.
HTML elements are the building blocks of HTML pages. With HTML constructs, images
and other objects such as interactive forms may be embedded into the rendered page. HTML
provides a means to create structured documents by denoting structural semantics for text
such as headings, paragraphs, lists, links, quotes and other items. HTML elements are
delineated by tags, written using angle brackets. Tags such as <img /> and <input /> directly
introduce content into the page. Other tags such as <p> surround and provide information
about document text and may include other tags as sub-elements. Browsers do not display the
HTML tags, but use them to interpret the content of the page.
  
CSS
  
CSS is used to define styles for your web pages, including the design, layout and variations in
display for different devices and screen sizes.
  
CSS is designed to enable the separation of presentation and content, including layout, colors,
and fonts. This separation can improve content accessibility, provide more flexibility and
control in the specification of presentation characteristics, enable multiple web pages to share
formatting by specifying the relevant CSS in a separate .css file which reduces complexity and
repetition in the structural content as well as enabling the .css file to be cached to improve the
page load speed between the pages that share the file and its formatting.
  
Separation of formatting and content also makes it feasible to present the same markup page in
different styles for different rendering methods, such as on-screen, in print, by voice (via
speech-based browser or screen reader), and on Braille-based tactile devices. CSS also has
rules for alternate formatting if the content is accessed on a mobile device.
The name cascading comes from the specified priority scheme to determine which style rule
applies if more than one rule matches a particular element. This cascading priority scheme is
predictable.
  
The CSS specifications are maintained by the World Wide Web Consortium (W3C). Internet
media type (MIME type) text/css is registered for use with CSS by RFC 2318 (March 1998).
The W3C operates a free CSS validation service for CSS documents.
  
 JavaScript:
  
JavaScript is a text-based programming language used both on the client-side and server-side
that allows you to make web pages interactive. Where HTML and CSS are languages that give
structure and style to web pages, JavaScript gives web pages interactive elements that engage
a user.
  
Alongside HTML and CSS, JavaScript is one of the core technologies of the World Wide Web.
Over 97% of websites use it client-side for web page behaviour, often incorporating third-party
libraries. All major web browsers have a dedicated JavaScript engine to execute the code on
the user's device.
  
As a multi-paradigm language, JavaScript supports event-driven, functional, and imperative
programming styles. It has application programming interfaces (APIs) for working with text,
dates, regular expressions, standard data structures, and the Document Object Model (DOM).
The ECMAScript standard does not include any input/output (I/O), such as networking,
storage, or graphics facilities. In practice, the web browser or other runtime system provides
JavaScript APIs for I/O.
  
JavaScript engines were originally used only in web browsers, but they are now core
components of other software systems, most notably servers and a variety of applications.
Although there are similarities between JavaScript and Java, including language name, syntax,
and respective standard libraries, the two languages are distinct and differ greatly in design.
  
 PHP
  
PHP started out as a small open source project that evolved as more and more people found
out how useful it was. Rasmus Lerdorf unleashed the first version of PHP way back in 1994.
PHP is a recursive acronym for "PHP: Hypertext Pre-processor".
  
PHP is a server side scripting language that is embedded in HTML. It is used to manage
dynamic content, databases, session tracking, even build entire e-commerce sites.
It is integrated with a number of popular databases, including MySQL, PostgreSQL, Oracle,
Sybase, Informix, and Microsoft SQL Server.
  
  
PHP is pleasingly zippy in its execution, especially when compiled as an Apache module on
the Unix side. The MySQL server, once started, executes even very complex queries with
huge result sets in record-setting time.
PHP supports a large number of major protocols such as POP3, IMAP, and LDAP. PHP4

added support for Java and distributed object architectures (COM and CORBA), making n-
tier development a possibility for the first time.

PHP is forgiving: PHP language tries to be as forgiving as possible.
  
 Flask
  
Flask is an API of Python that allows us to build up web-applications. It was developed by
Armin Ronacher. Flask’s framework is more explicit than Django’s framework and is also

easier to learn because it has less base code to implement a simple web-Application. A Web-
Application Framework or Web Framework is the collection of modules and libraries that

helps the developer to write applications without writing the low-level codes such as
protocols, thread management, etc. Flask is based on WSGI (Web Server Gateway Interface)
toolkit and Jinja2 template engine.
  
  
