
**Software Requirements Specification**

**for**

**Volunteer Management System**

**Version 3.0 approved**

**Prepared by Michael Nolander, Desmond Mack, Chris Coulthard**

**SENG 3130**

**November 28, 2022**
***Copyright © 1999 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document.***
***Software Requirements Specification for Volunteer Management System	Page*** 

**Table of Contents**

[**1. Introduction](#_heading=h.1fob9te)	**1****

[1.1 Purpose](#_heading=h.3znysh7)	1

[1.2 Document Conventions](#_heading=h.pjph0n7e39qy)	1

[1.3 Intended Audience and Reading Suggestions](#_heading=h.c4osq885r415)	1

[1.4 Product Scope](#_heading=h.6yx2wljustti)	1

[1.5 References](#_heading=h.plk04vhf3qd7)	1

[**2. Overall Description](#_heading=h.k3ifb3nv0yt3)	**1****

[2.1 Product Perspective](#_heading=h.2s8eyo1)	1

[2.2 Product Functions](#_heading=h.9pq09jdzlse0)	2

[2.3 User Classes and Characteristics](#_heading=h.djamipd43vl)	3

[2.4 Operating Environment](#_heading=h.sykatqjn3d7e)	4

[2.5 Design and Implementation Constraints](#_heading=h.yqwrv1hc2bg9)	4

[2.6 User Documentation](#_heading=h.hki2xesutt40)	4

[2.7 Assumptions and Dependencies](#_heading=h.s3mdhqdbv6ko)	4

[**3. External Interface Requirements](#_heading=h.t0kfkhgjq6k4)	**5****

[3.1 User Interfaces](#_heading=h.2jxsxqh)	5

[3.2 Hardware Interfaces](#_heading=h.wpq9rbbdtdj0)	6

[3.3 Software Interfaces](#_heading=h.gm1hlw49qj49)	6

[3.4 Communications Interfaces](#_heading=h.sdk4jzeccb0n)	6

[**4. System Features](#_heading=h.jj02vhinceu7)	**7****

[**5. Other Nonfunctional Requirements](#_heading=h.3whwml4)	**7****

[5.1 Performance Requirements](#_heading=h.2bn6wsx)	7

[5.2 Safety Requirements](#_heading=h.oh2dxsvaqsv9)	8

[5.3 Security Requirements](#_heading=h.j355kia5lw8)	8

[5.4 Software Quality Attributes](#_heading=h.392cs6z4bafu)	8

[5.5 Business Rules](#_heading=h.iv7er9jux8o)	8

[**6. Other Requirements](#_heading=h.ifq1yhklngb6)	**8****






**Revision History**

|**Name**|**Date**|**Reason For Changes**|**Version**|
| :- | :- | :- | :- |
|Final|Nov. 28/22|All sections completed|3.0|
|Partial|Nov. 7/22|Sections 1-4 completed|2.0|
|Template|Nov. 3/22|Document created|1.0|



***Software Requirements Specification for Volunteer Management System	Page*** 
1. # **Introduction**
   1. ## **Purpose** 
The purpose of this SRS is to describe the software requirements specifications for the first version of the Volunteer Management System. This application will allow volunteers to be assigned to assistance requests and will organize case history. This document will pertain to the initial release of the system.
1. ## **Document Conventions**
There are no standard conventions used in this document.
1. ## **Intended Audience and Reading Suggestions**
This document is written for developers and testers. 
1. ## **Product Scope**
Our company seeks to provide an efficient and straightforward way that will connect senior aid volunteers to those who are in need of the service. This service should streamline the application process for those in the city providing administrative duties and have the capacity to later be used for other volunteer opportunities.
1. ## **References**
This document does not reference any other documents.
\*

1. # **Overall Description**
   1. ## **Product Perspective**
This system will provide a service that will connect seniors who need help around the house with

volunteers in a much faster manner than the current system which is all done by hand. As well, it will automatically provide background checks so that want to be volunteers can start in approximately 3 days opposed to the current ten days. This system will also have the ability to be expanded so that students can connect to additional tutors outside of their online program.


1. ## **Product Functions**

|**Volunteer.Create**|**Create New Volunteers**|
| :- | :- |
|`        `.ReceiveDetails|The VMS shall receive the details of the volunteer, including their full name and other information.|
|`                `.Exists|If a volunteer with the exact same details already exists in the system, the new volunteer is denied. The VMS shall notify the administrator that a duplicate volunteer was attempted to be created.|
|`        `.BackgroundCheck|The VMS shall take the volunteer’s information and send it to the police department to complete a background check.|
|`        `.AssignNumber|The VMS shall generate a unique volunteer number for the volunteer.|


|**Volunteer.Assign**|**Assign Volunteer**|
| :- | :- |
|`        `.GetRequest|An elderly individual inputs a request for services with a description or calls a service worker who inputs the information for them.|
|`        `.CheckAvailability|The system checks the availability that is posted by volunteers.|
|`                `.CompareTimes|The system then cross references the availability with the times the services are required.|
|`                        `.Multiple|If there are multiple people with availability during the time that the services are required, it will then check which volunteers' preference best matches the request description.|
|`        `.SendRequest|The system then sends a request to the selected volunteer with the details. |
|`        `.ReceiveRequest|The volunteer then replies with a confirmation of the task or declines. If declined it loops back to the availability step and repeats the following steps|
|`        `.SendConfirmation|Once the volunteer has accepted the system sends a confirmation email with a calendar reminder attachment. |




|**DailyReport.Generate**|**Generate Daily Report**|
| :- | :- |
|`        `.EndOfDay|The specified End-of-Day time has been reached.|
|`                `.CollectCurrentDayCases|The VMS shall collect all the cases for the current day.|
|`                `.CollectPastCases|The VMS shall collect case data from the past.|
|`                `.GenerateForecast|The VMS shall consider the current day case data as well as past case data to help formulate a forecast for the next week’s case numbers.|
|`                `.DisplayReport|The VMS shall display the generated report of the current day’s cases, along with the next week’s forecast information.|

1. ## **User Classes and Characteristics**
● Volunteers (favoured) - Approved users who have submitted their information into the

system and can volunteer for requests. This also includes the student-peers and

senior-peers, who get assigned to specific people in need of volunteer work.

● Volunteer Administrators (favoured) - Users with higher privileges who can approve

new volunteers, view volunteer statistics, and assign volunteers to cases.

● SPCC staff (favoured) - Employees in the Senior People Care Centre who receive

senior people’s information and create profiles for them in the Volunteer Management

System.

● School Staff (ignored) - Or school administrators; users who submit requests to the

Volunteer Management System on behalf of students.

Indirect user classes

● Seniors (favoured) - Users who request volunteer work by calling the SPCC and

are assigned a senior-peer.

● Police Officers (ignored) - Manually approve background checks in the background

check system to validate new volunteers.

Disfavoured user classes

● Students (indirect) - Request teaching assistance to the school staff and are assigned

a student-peer.

● Unapproved Volunteers (direct) - Users who have not been approved and have not

completed a background check; are not allowed to access the system.
1. ## **Operating Environment**
Our system will work cross-platform on Android and iOS as a mobile application, with the oldest supported version of each operating system being the oldest possible supported version depending on dependencies and Apple/Google support; Guaranteed support for operating systems released in the last three (3) years. All versions of the application will be supported for 6 months before requiring the user to update to ensure security and stability. The application will work directly with the volunteer database and Background Check System.
1. ## **Design and Implementation Constraints**
Our design seeks to avoid any instances where it will be limited by outside sources, but this cannot be avoided entirely. We have to interface with the police background check system, which will be the limiting factor on how fast we can process new volunteers. The other constraint we must take into consideration is that many older citizens struggle to use new technology, so the request system must be straightforward and clear. This results in more steps to place a request so that the process is easy to follow. Our system will also ensure large instructional sections that will contain larger than standard font sizes for those who are starting to lose some of their vision.
1. ## **User Documentation**
Once the user creates an account, the mobile app will walk them through the core features of the application. There will also be a screen that provides additional help such as: 

- Repeating the Tutorial
- Getting to know Additional Features
- Contacting the Help-Desk
  1. ## **Assumptions and Dependencies**
Assumptions

● “We do not have actual figures, but it is estimated around 10K to 15K cases.”

● “Engaging people in beneficial activities can reduce the crime rate at the city, which is expected

to eventually increases the business transactions at the Downtown area and local shops

with 10%.”

Dependencies

● Automatic police certificate check system, system depends on this as every volunteer needs to

complete a check using the system

● Online teaching services used by students, which is an alternative to the volunteer system which

can reduce the load on the new system
1. # **External Interface Requirements**
   1. ## **User Interfaces**
![](Aspose.Words.5035aac1-2b61-4001-ada1-243b8691026c.001.jpeg)

*Sketch of “Assign Volunteer” and “Create Volunteer” pages of VMS application*

![](Aspose.Words.5035aac1-2b61-4001-ada1-243b8691026c.002.jpeg)

*Sketch of “Search Volunteer” page of VMS application*
1. ## **Hardware Interfaces**
No hardware interfaces have been identified for the Volunteer Management System.
1. ## **Software Interfaces**
![](Aspose.Words.5035aac1-2b61-4001-ada1-243b8691026c.003.png)

*Ecosystem map for Volunteer Management System*
1. ## **Communications Interfaces**
- **CI-1:** The Volunteer Management System shall send a text message or email (depending on user settings) to the volunteer when they have been assigned to a case.
- **CI-2:** The Volunteer Management System shall send a text message or email (depending on user settings) to the person who requested a volunteer when a volunteer is coming to assist them.
1. # **System Features**
![](Aspose.Words.5035aac1-2b61-4001-ada1-243b8691026c.004.png)

*Feature tree for Volunteer Management System*
1. # **Other Nonfunctional Requirements**
   1. ## **Performance Requirements**
- **PER-1:** In the first year, the system should track 60% of the senior cases in the city. 
- **PER-2:** In the first year, the system should provide support to 85% of the reported cases. 
- **PER-3:** The system should also reduce the amount of time it takes to process the volunteers through background checks and other administrative duties.
  1. ## **Safety Requirements**
- **SAF-1:** Every verified volunteer must undergo a background check following local police regulations before being added to the system.
  1. ## **Security Requirements**
- **SEC-1:** The personal information of both the volunteers and the people in need of assistance should be kept confidential
- **SEC-2:** The information that goes through the police to do the background checks should not be compromised.
- **SEC-3:** No volunteer who has not been through the background checks should get access to volunteer requests.
  1. ## **Software Quality Attributes**
- **Interoperability** - The Volunteer Management System shall work with the Background Check System.
- **Security** - Student and Senior Personal Data shall not be shown to volunteers unless they’re selected for the volunteer job.
- **Durability** - The Volunteer Management System shall keep volunteer activity data for two (2) years.
- **Accessibility** - The Volunteer Management System shall be easy enough for seniors to use.
  1. ## **Business Rules**
- **BUR-1:** An Increase in people applying to become a volunteer / An Increase in available volunteers
- **BUR-2:** Reduced complexity of application/approval process 
- **BUR-3:** Reduction in time for a volunteer to be assigned to a volunteer request 
1. # **Other Requirements**
No other requirements have been identified for the Volunteer Management System.


**Appendix A: Glossary**

|**Term**|**Definition**|
| :- | :- |
|VMS|Volunteer Management System|
|SPCC|Senior People Care Center|
|Case|Assistance request assigned to one volunteer|

**Appendix B: Analysis Models**

![](Aspose.Words.5035aac1-2b61-4001-ada1-243b8691026c.005.png)

*Entity-relationship diagram for Volunteer Management System*



|**Data Element**|**Description**|**Composition / Data Type**|**Length**|**Values**|
| :- | :- | :- | :- | :- |
|Volunteer details|Name and information about volunteer|<p>Volunteer name</p><p>+ Volunteer number</p>|||
|Volunteer name|Name of volunteer|String|50|Lower-case or upper-case alphabetic characters, and periods|
|Request location|Address of the location where assignment will take place|String|20|Alphanumeric characters|
|Request ID|Unique numeric identifier for request|Integer|10|Sequence generated by system, starting at 1|
|Requester details|Name and information about requester|<p>Requester name</p><p>+ Request ID</p><p>+ Request location</p>|||
|Requester name|Name of requester|String|50|Lower-case or upper-case alphabetic characters, and periods|
*Data dictionary for Volunteer Management System*

**Appendix C: To Be Determined List**

There are no TBD references remaining for this document.
