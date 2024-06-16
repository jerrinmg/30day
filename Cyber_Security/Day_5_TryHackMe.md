# Day 5:   Web Application Security
## A. Introduction
Web application : Program that runs on the server. 
Server = Serves customer continously

Some examples: 
1. Webmail : Gmail, Tutanota, Prtotonmail
2. Online office suittes : Microsoft Office 365, Google Drive, and Zoho office
3. Online shoppoing such as Amazon 

. A database is used to store information in an organized way.


    *Products database: This database contains details about the products, such as name, images, specifications, and price.
    *Customers database: It contains all details related to customers, such as name, address, email, and phone number.
    *Sales database: We expect to see what each customer has purchased and how they paid in this database.



### Attacking an Shopping Website
![image](https://github.com/jerrinmg/30day/assets/166682032/19e6b9a9-e86d-4be8-bac9-e8e84a6161b4)

General functions that are done when using an web application. 
![image](https://github.com/jerrinmg/30day/assets/166682032/958d58d6-b330-4379-94c1-124b6883c5aa)

1. The user enters an item name or related keywords in the search field. The web browser sends the search keyword(s) to the online shopping web application.
2. The web application queries (searches) the products database for the submitted keywords.
3. The product database returns the search results matching the provided keywords to the web application.
4. The web application formats the results as a friendly web page and returns them to the user.


## Web Application Security Risks
![image](https://github.com/jerrinmg/30day/assets/166682032/fd1d75b6-6cf4-495d-8d4c-e46d44ee1eae)



**Common Attacks Against Web Applications**

* **Login**: Brute force attacks to discover passwords
* **Search**: Injection attacks to breach the system or execute unauthorized code
* **Payment**: Checking for cleartext or weak encryption of payment details

**OWASP Top Ten**

* **Identification and Authentication Failure**:
	+ Allowing brute force attacks
	+ Allowing weak passwords
	+ Storing passwords in plain text
* **Broken Access Control**:
	+ Failing to apply least privilege principle
	+ Allowing access to unauthorized resources
	+ Allowing unauthorized browsing of authenticated pages
* **Injection**:
	+ Lack of proper validation and sanitization of user input
* **Cryptographic Failures**:
	+ Sending sensitive data in clear text
	+ Relying on weak cryptographic algorithms
	+ Using default or weak keys for cryptographic functions



## Practical Example of Web Application Security


   ![image](https://github.com/jerrinmg/30day/assets/166682032/6ce06947-0ca1-4304-b258-1c54a635838c)


# Exploiting Insecure Direct Object Reference (IDOR) Vulnerability

## Introduction
In this task, I investigated a vulnerable website with an Insecure Direct Object Reference (IDOR) vulnerability, which falls under the category of Broken Access Control. IDOR vulnerabilities occur when a web application fails to validate user permissions and allows unauthorized access to restricted resources or actions.

## Exploitation
Upon examining the website's Inventory Management System, I noticed that an attacker had sabotaged the system by assigning the wrong tires to each assembly line. To undo the attacker's actions, I exploited the IDOR vulnerability present on the website.

The vulnerability allowed me to access restricted resources by modifying the `id` parameter in the URL. By changing the `id` value, I could potentially access resources intended for other users or privileged roles.

### Steps
1. Analyzed the URL structure: `https://example.com/resource?id=X`
2. Identified that the `id` parameter was likely used to retrieve specific resources.
3. Attempted to access different resources by incrementing or decrementing the `id` value.
4. Discovered that setting `id=7` granted me access to the Database administrator's control panel.

## Impact
By exploiting the IDOR vulnerability and accessing the administrator's control panel, I could:
- View sensitive information intended for privileged users.
- Modify critical data, such as tire assignments for assembly lines.
- Potentially perform other unauthorized actions with elevated privileges.

## Mitigation
To mitigate the IDOR vulnerability, the web application should implement proper access control measures, such as:
- Validating user permissions before allowing access to resources.
- Avoiding the use of sequential or predictable identifiers for sensitive resources.
- Implementing role-based access control (RBAC) to restrict access based on user roles and privileges.
- Logging and monitoring suspicious activity, such as attempts to access unauthorized resources.

## Conclusion
The Insecure Direct Object Reference (IDOR) vulnerability allowed me to bypass intended access restrictions and perform unauthorized actions on the vulnerable website. By exploiting this vulnerability, I could undo the attacker's sabotage and potentially access or modify other sensitive resources. Proper access control measures must be implemented to prevent such vulnerabilities and protect the confidentiality, integrity, and availability of web applications and their data.
![image](https://github.com/jerrinmg/30day/assets/166682032/6a56d31b-8ad9-48f7-ae87-f5675af97b30)



