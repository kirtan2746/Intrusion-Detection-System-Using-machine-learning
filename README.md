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
# Software Platform 

Python, a free and open-source object-oriented programming language, draws 
attention with its simple syntax and dynamic structure. In Python, it's very easy to 
write code and analyse code. Another advantage is that it has the advantage of 
extensive documentation (books, internet sites, forums, etc.). In addition to all these 
advantages, it works in concert with many libraries which "machine learning" 
applications can be done. In this context, Python3.7 has been chosen to be used in 
this work, because of many of the advantages it provides[25]. 
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
operations quickly and easily, has been used in calculations in this work[26]. 
Hardware Platform 
An evaluation criterion for machine learning algorithms is the execution time. 
However, the execution time may vary depending on the performance of the 
computer being used. Because of this, the technical specifications of the computer 
used in the application are shared. The technical characteristics of the computer used 
in the implementation phase are
