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
