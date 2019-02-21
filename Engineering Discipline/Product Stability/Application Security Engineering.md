# Application Security Engineering

This document describes application security engineering best practices and guidelines that can be integrated into the software development project to improve the security posture of software products.

## Threat Modeling 
Threat modeling is an approach for analyzing the security threats of an application. It is a structured approach that enables you to identify, quantify, and address the security risks associated with an application.
<p align="center">
<img width="263" alt="threat modeling" src="https://user-images.githubusercontent.com/5235310/53144255-8d792d80-35c1-11e9-97a1-d991bdd8c59f.png">
</p>

The following example shows a threat modeling of user login page.
<p align="center">
<img width="387" alt="example threat model" src="https://user-images.githubusercontent.com/5235310/53144086-d11f6780-35c0-11e9-8894-fe21199b08ff.png">
</p>
Source: OWASP

Let's create a threat model based on a case study. Consider the following case.
* A Norway based professional company uses a software application which can allow users to book professionals (Electrician, Plumber) and request professional services through the company.
* They wanted a new feature in this application which can allow users to upload and download property documents and maintenance documents. Access to these documents must be strictly restricted to relevant users.
* Since last week, the dev team is designing the new feature for the website, that will enable authenticated users to upload and download property documents.
* The architects will reuse the existing infrastructure whenever possible (they already have user accounts).
* One of the board members got to know about these cyber attackers and the crazy attacks they perform which can easily damage the business and its reputation.
* He also heard about the threat modeling which helps project teams to identify major threats and take necessary security measures before they even start implementation.
* He wanted to assess the threats and security of his product.

The following data flow diagram can be derived based on the communication among components.
![threatmodel](https://user-images.githubusercontent.com/5235310/53144331-da5d0400-35c1-11e9-8a9c-20c7045d4c89.jpeg)

Let's think about what can go wrong.
We can use Microsoft's STRIDE model to identify the threats of this application.
Microsoft's STRIDE Model:
* Spoofing - Impersonate User
* Tampering - Maliciously change/modify persistent data, such as persistent data in a database, and the alteration of data in transit
* Repudiation - Perform an illegal action and deny it.
* Information Disclosure - Read a file that one was not granted access to, or to read data in transit
* Denial of Service - Deny access to valid users
* Elevation of Privilege - Gain privileged access or gain unauthorized access

Based on the above model, let's identify the issues that can be threaten the security of the application.
![threatmodel 1](https://user-images.githubusercontent.com/5235310/53144381-0e382980-35c2-11e9-92d0-cb177566447e.jpeg)

Threat modeling can also be done at the end of software development. But this approach is costly since we may need to change existing systems and components to mitigate security risks identified from threat modeling.

The threat modeling process of an already built software application can be decomposed into 3 high level steps:
* Step 1:Decompose the Application
* Step 2:Determine and rank threats
* Step 3:Determine countermeasures and mitigation


