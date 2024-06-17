# Day 6:   Introduction to Pentesting
## A. Pentesting Fundamentals

What is Penetration Testing?
A Penetration test or pentest is an ethically-driven attempt to test and analyse the security defences to protect these assets and pieces of information. A penetration test involves using the same tools, techniques, and methodologies that someone with malicious intent would use and is similar to an audit.

![image](https://github.com/jerrinmg/30day/assets/166682032/6c162859-0835-4c5a-94d0-4590c2bcd1a7)




### Different Types of Hackers
![image](https://github.com/jerrinmg/30day/assets/166682032/14625184-6e29-4a25-8ae7-d7f018587e3c)

### Rules of Engagement (ROE)
The ROE is a document that is created at the initial stages of a penetration testing engagement. This document consists of three main sections (explained in the table below), which are ultimately responsible for deciding how the engagement is carried out. The SANS institute has a great example of this document which you can view online here.

![image](https://github.com/jerrinmg/30day/assets/166682032/73a15b34-3e4e-465f-b6d4-b923ca106f31)



## Penetration Testing Methodologies


| Stage | Description |
| --- | --- |
| Information Gathering | This stage involves collecting as much publically accessible information about a target/organisation as possible, for example, OSINT and research. Note: This does not involve scanning any systems. |
| Enumeration/Scanning | This stage involves discovering applications and services running on the systems. For example, finding a web server that may be potentially vulnerable. |
| Exploitation | This stage involves leveraging vulnerabilities discovered on a system or application. This stage can involve the use of public exploits or exploiting application logic. |
| Privilege Escalation | Once you have successfully exploited a system or application (known as a foothold), this stage is the attempt to expand your access to a system. You can escalate horizontally and vertically, where horizontally is accessing another account of the same permission group (i.e. another user), whereas vertically is that of another permission group (i.e. an administrator). |
| Post-exploitation | This stage involves a few sub-stages:<br>1. What other hosts can be targeted (pivoting)<br>2. What additional information can we gather from the host now that we are a privileged user<br>3. Covering your tracks<br>4. Reporting |



### OSSTMM Open Source Security Testing Methodology Manual 
![image](https://github.com/jerrinmg/30day/assets/166682032/84c9e36b-b265-4b5d-aace-df8b9d6ad95d)

![image](https://github.com/jerrinmg/30day/assets/166682032/515f5380-972a-4dd7-b391-5a4c5c100e00)

### OWASP Open Web Application Security Project

![image](https://github.com/jerrinmg/30day/assets/166682032/515f5380-972a-4dd7-b391-5a4c5c100e00)
![image](https://github.com/jerrinmg/30day/assets/166682032/6edb4285-3376-4ad6-a470-4481d1c8b3c5)

### NIST Cybersecurity Framework 1.1
The NIST Cybersecurity Framework is a popular framework used to improve an organisations cybersecurity standards and manage the risk of cyber threats. This framework is a bit of an honourable mention because of its popularity and detail.

The framework provides guidelines on security controls & benchmarks for success for organisations from critical infrastructure (power plants, etc.) all through to commercial.  There is a limited section on a standard guideline for the methodology a penetration tester should take.


![image](https://github.com/jerrinmg/30day/assets/166682032/55fafc8a-9749-4997-a31c-22a01ec445da)

### NCSC CAF National Cyber Security Centre  Cyber Assessment Framework 
The Cyber Assessment Framework (CAF) is an extensive framework of fourteen principles used to assess the risk of various cyber threats and an organisation's defences against these.



The framework applies to organisations considered to perform "vitally important services and activities" such as critical infrastructure, banking, and the likes. The framework mainly focuses on and assesses the following topics:

Data security

System security

Identity and access control

Resiliency

Monitoring

Response and recovery planning


![image](https://github.com/jerrinmg/30day/assets/166682032/8c3aaa2b-4add-4f8c-8b6b-1db86cc3066a)


