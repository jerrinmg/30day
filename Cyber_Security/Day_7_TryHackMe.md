# Day 7:   Introduction to Pentesting
## A. Pentesting Fundamentals

### Black box, White box, Grey box Penetration Testing
![image](https://github.com/jerrinmg/30day/assets/166682032/4aa5540d-0bfa-4508-aef3-b435e333fada)
**Three Primary Scopes of Testing**
=====================================

When testing an application or service, there are three primary scopes to consider. The scope you choose will depend on your understanding of the target and the level of testing required.

### Black-Box Testing

* No knowledge of internal workings
* Tester acts as a regular user
* Interacts with interface to test functionality
* No programming knowledge required
* Increases time spent on information gathering and enumeration
* High-level process

### Grey-Box Testing

* Combination of black-box and white-box testing
* Tester has limited knowledge of internal components
* Interacts with application like a black-box scenario
* Uses knowledge to resolve issues as they arise
* Saves time compared to black-box testing
* Popular choice for penetration testing

### White-Box Testing

* Low-level process
* Tester has full knowledge of internal components
* Tests internal components and application logic
* Requires programming knowledge
* More time-consuming than black-box testing
* Guarantees entire attack surface can be validated

### Practical:  ACME Penetration Test
ACME has approached you for an assignment. They want you to carry out the stages of a penetration test on their infrastructure. View the site (by clicking the green button on this task) and follow the guided instructions to complete this exercise.
![image](https://github.com/jerrinmg/30day/assets/166682032/ae77baf9-ef41-4df2-8ee5-2bf808562862)


### Weakness / Info Gathering 
The information gathering stage of an engagement is often undervalued. This stage involves using publicly accessible channels to collect intel on your target.

Abbey, who has a public profile on LinkedIn, advertises that she works for ACME and even includes her email in her bio, which is a possible way we can target her work laptop and thus the
![image](https://github.com/jerrinmg/30day/assets/166682032/075cec6d-eb9b-4846-b174-f73a1e6b55f1)


###  Enumeration & Scanning
The goal of this stage is to get a complete picture of your target. A penetration tester will try to identify user accounts, machines on their network, network shares, applications etc. Information gathered from stage 2, and the engagement scope document will help in enumerating your target.

The enumeration phase is very important as your findings are used to exploit your target's systems (stage 4).

Let's pretend Abbey from stage 2 made a post on LinkedIn sharing a blog post she wrote about ACME. From this post, you find ACME's web server's IP "96.37.50.151"; try scanning it.
![image](https://github.com/jerrinmg/30day/assets/166682032/774bf0d6-576a-4a47-8131-5fee7d2ad755)


### 4. Exploitation
Exploitation is the use of a vulnerability discovered to gain un-authorised access to an information security system or data.
From stage 3 we found there are vunlerbilities. Using that we use the tool metaexploit.
![image](https://github.com/jerrinmg/30day/assets/166682032/1b45034f-2c35-41f8-b7fe-77dfd9646c57)


### 5.  Post Exploitation
Exploitation is the use of a vulnerability discovered to gain un-authorised access to an information security system or data.
From stage 3 we found there are vunlerbilities. Using that we use the tool metaexploit.


![image](https://github.com/jerrinmg/30day/assets/166682032/e76e2ca5-42c4-4c18-80f8-1117bc048c83)

### 6. Pentest Report & Clearing-up
This stage usually occurs at the end of a penetration test. As a penetration tester, you will have to explain the results of your engagement to the client. This is usually done in the form of a report that contains details regarding any security issues you’ve found and how to mitigate them. The client will use this report to understand the security issues and fix the flaws in the technology stack that was tested.

It’s also best practice to clean up the environment you’ve been testing (where possible). For example, if you were provided access to machines or tooling by the client, you need to delete any artefacts that have been created as a result of testing.
![image](https://github.com/jerrinmg/30day/assets/166682032/ae15719e-6bcf-4ed4-af37-f5f1b788e0de)

## A. Result Finished Pentesting Fundamentals
![image](https://github.com/jerrinmg/30day/assets/166682032/52a8261e-b080-4f13-bdc1-3a4e4979e5a7)
