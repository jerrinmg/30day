# Day 1: Platform

Decided to learn about cyber security on the TryHackMe website. 

## A. Intro to Offensive Security  

1."GoBuster" to brute-force FakeBank's website to find hidden directories and pages. GoBuster will take a list of potential page or directory names and tries accessing a website with each of them; if the page exists, it tells you.

2. Find hidden website pages: eg admin portal, for bank for the admin to transfer money.
    ```bash
   gobuster -u http://fakebank.com -w wordlist.txt dir
   ```

![image](https://github.com/jerrinmg/30day/blob/1b814ad924651e7f7fc57b77f96f8e7137068fe0/images/day%201%20screenshot%201.png)
   

4. Hack the bank !

You should have found a secret bank transfer page that allows you to transfer money between accounts at the bank (/bank-transfer). Type the hidden page into the FakeBank website on the machine.

   ```bash
   www.fakebank/bank-transfer
   ```


## Success!
We transferred 767 $ dollars from the FAKE Bank to our account! 

 ![image](https://github.com/jerrinmg/30day/blob/1b814ad924651e7f7fc57b77f96f8e7137068fe0/images/Screenshot%20from%202024-06-04%2000-00-23.png)


## Knowledge
* GoBuster tool!
