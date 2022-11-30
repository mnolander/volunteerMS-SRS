
# **Software Requirements Specification for Volunteer Management System**

**Version 3.0 approved**

**Prepared by Michael Nolander, Desmond Mack, Chris Coulthard**

**SENG 3130**

**November 30, 2022**

|**Table of Contents**|
|:-|
|[**1. Introduction**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#1-introduction)|
|[1.1 Purpose](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#11-purpose)|
|[1.2 Document Conventions](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#12-document-conventions)|
|[1.3 Intended Audience and Reading Suggestions](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#13-intended-audience-and-reading-suggestions)|
|[1.4 Product Scope](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#14-product-scope)|
|[1.5 References](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#15-references)|
|[**2. Overall Description**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#2-overall-description)|
|[2.1 Product Perspective](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#21-product-perspective)|
|[2.2 Product Functions](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#22-product-functions)|
|[2.3 User Classes and Characteristics](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#23-user-classes-and-characteristics)|
|[2.4 Operating Environment](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#24-operating-environment)|
|[2.5 Design and Implementation Constraints](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#25-design-and-implementation-constraints)|
|[2.6 User Documentation](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#26-user-documentation)|
|[2.7 Assumptions and Dependencies](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#27-assumptions-and-dependencies)|
|[**3. External Interface Requirements**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#3-external-interface-requirements)|
|[3.1 User Interfaces](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#31--user-interfaces)|
|[3.2 Hardware Interfaces](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#32-hardware-interfaces)|
|[3.3 Software Interfaces](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#33-software-interfaces)|
|[3.4 Communications Interfaces](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#34-communications-interfaces)|
|[**4. System Features**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#4-system-features)|
|[**5. Other Nonfunctional Requirements**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#5-other-nonfunctional-requirements)|
|[5.1 Performance Requirements](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#51-performance-requirements)|
|[5.2 Safety Requirements](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#52-safety-requirements)|
|[5.3 Security Requirements](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#53-security-requirements)|
|[5.4 Software Quality Attributes](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#54-software-quality-attributes)|
|[5.5 Business Rules](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#55-business-rules)|
|[**6. Other Requirements**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#6-other-requirements)|
|[**Appendix A: Glossary**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#appendix-a-glossary)|
|[**Appendix B: Analysis Models**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#appendix-b-analysis-models)|
|[**Appendix C: To Be Determined List**](https://github.com/mnolander/volunteerMS-SRS/edit/main/SENG%203130%20Assignment%203_4%20-%20SRS%20Document.md#appendix-c-to-be-determined-list)|


**Revision History**

|**Name**|**Date**|**Reason For Changes**|**Version**|
| :- | :- | :- | :- |
|Final|Nov. 28/22|All sections completed|3.0|
|Partial|Nov. 7/22|Sections 1-4 completed|2.0|
|Template|Nov. 3/22|Document created|1.0|

# 1. **Introduction**
   ## 1.1 **Purpose** 
The purpose of this SRS is to describe the software requirements specifications for the first version of the Volunteer Management System. This application will allow volunteers to be assigned to assistance requests and will organize case history. This document will pertain to the initial release of the system.  

## 1.2 **Document Conventions**
There are no standard conventions used in this document.

## 1.3 **Intended Audience and Reading Suggestions**
This document is written for developers and testers. 

## 1.4 **Product Scope**
Our company seeks to provide an efficient and straightforward way that will connect senior aid volunteers to those who are in need of the service. This service should streamline the application process for those in the city providing administrative duties and have the capacity to later be used for other volunteer opportunities.

## 1.5 **References**
This document does not reference any other documents.

# 2. **Overall Description**
## 2.1 **Product Perspective**
This system will provide a service that will connect seniors who need help around the house with volunteers in a much faster manner than the current system which is all done by hand. As well, it will automatically provide background checks so that want to be volunteers can start in approximately 3 days opposed to the current ten days. This system will also have the ability to be expanded so that students can connect to additional tutors outside of their online program.


## 2.2 **Product Functions**

|**Volunteer.Create**|**Create New Volunteers**|
| :- | :- |
|        .ReceiveDetails|The VMS shall receive the details of the volunteer, including their full name and other information.|
|                .Exists|If a volunteer with the exact same details already exists in the system, the new volunteer is denied. The VMS shall notify the administrator that a duplicate volunteer was attempted to be created.|
|        .BackgroundCheck|The VMS shall take the volunteer’s information and send it to the police department to complete a background check.|
|        .AssignNumber|The VMS shall generate a unique volunteer number for the volunteer.|


|**Volunteer.Assign**|**Assign Volunteer**|
| :- | :- |
|        .GetRequest|An elderly individual inputs a request for services with a description or calls a service worker who inputs the information for them.|
|        .CheckAvailability|The system checks the availability that is posted by volunteers.|
|                .CompareTimes|The system then cross references the availability with the times the services are required.|
|                        .Multiple|If there are multiple people with availability during the time that the services are required, it will then check which volunteers' preference best matches the request description.|
|        .SendRequest|The system then sends a request to the selected volunteer with the details. |
|        .ReceiveRequest|The volunteer then replies with a confirmation of the task or declines. If declined it loops back to the availability step and repeats the following steps|
|        .SendConfirmation|Once the volunteer has accepted the system sends a confirmation email with a calendar reminder attachment. |


|**DailyReport.Generate**|**Generate Daily Report**|
| :- | :- |
|        .EndOfDay|The specified End-of-Day time has been reached.|
|                .CollectCurrentDayCases|The VMS shall collect all the cases for the current day.|
|                .CollectPastCases|The VMS shall collect case data from the past.|
|                .GenerateForecast|The VMS shall consider the current day case data as well as past case data to help formulate a forecast for the next week’s case numbers.|
|                .DisplayReport|The VMS shall display the generated report of the current day’s cases, along with the next week’s forecast information.|

## 2.3 **User Classes and Characteristics**
● **Volunteers (favoured)** - Approved users who have submitted their information into the system and can volunteer for requests. This also includes the student-peers and senior-peers, who get assigned to specific people in need of volunteer work.

● **Volunteer Administrators (favoured)** - Users with higher privileges who can approve new volunteers, view volunteer statistics, and assign volunteers to cases.

● **SPCC staff (favoured)** - Employees in the Senior People Care Centre who receive senior people’s information and create profiles for them in the Volunteer Management System.

● **School Staff (ignored)** - Or school administrators; users who submit requests to the Volunteer Management System on behalf of students. 

Indirect user classes:

● **Seniors (favoured)** - Users who request volunteer work by calling the SPCC and are assigned a senior-peer.

● **Police Officers (ignored)** - Manually approve background checks in the background check system to validate new volunteers.

Disfavoured user classes:

● **Students (indirect)** - Request teaching assistance to the school staff and are assigned a student-peer.

● **Unapproved Volunteers (direct)** - Users who have not been approved and have not completed a background check; are not allowed to access the system.

## 2.4 **Operating Environment**
Our system will work cross-platform on Android and iOS as a mobile application, with the oldest supported version of each operating system being the oldest possible supported version depending on dependencies and Apple/Google support; Guaranteed support for operating systems released in the last three (3) years. All versions of the application will be supported for 6 months before requiring the user to update to ensure security and stability. The application will work directly with the volunteer database and Background Check System.

## 2.5 **Design and Implementation Constraints**
Our design seeks to avoid any instances where it will be limited by outside sources, but this cannot be avoided entirely. We have to interface with the police background check system, which will be the limiting factor on how fast we can process new volunteers. The other constraint we must take into consideration is that many older citizens struggle to use new technology, so the request system must be straightforward and clear. This results in more steps to place a request so that the process is easy to follow. Our system will also ensure large instructional sections that will contain larger than standard font sizes for those who are starting to lose some of their vision.

## 2.6 **User Documentation**
Once the user creates an account, the mobile app will walk them through the core features of the application. There will also be a screen that provides additional help such as: 

- Repeating the Tutorial
- Getting to know Additional Features
- Contacting the Help-Desk


## 2.7 **Assumptions and Dependencies**
Assumptions:

● “We do not have actual figures, but it is estimated around 10K to 15K cases.”

● “Engaging people in beneficial activities can reduce the crime rate at the city, which is expected to eventually increases the business transactions at the Downtown area and local shops with 10%.”

Dependencies:

● Automatic police certificate check system, system depends on this as every volunteer needs to complete a check using the system

● Online teaching services used by students, which is an alternative to the volunteer system which can reduce the load on the new system

# 3. **External Interface Requirements**
## 3.1  **User Interfaces**
![](https://github.com/mnolander/volunteerMS-SRS/blob/main/AssignCreate.jpeg?raw=true)

*Sketch of “Assign Volunteer” and “Create Volunteer” pages of VMS application*

![](https://github.com/mnolander/volunteerMS-SRS/blob/main/Search.jpeg?raw=true)

*Sketch of “Search Volunteer” page of VMS application*

## 3.2 **Hardware Interfaces**
No hardware interfaces have been identified for the Volunteer Management System.

## 3.3 **Software Interfaces**
![](https://github.com/mnolander/volunteerMS-SRS/blob/main/Ecosystem.png?raw=true)

*Ecosystem map for Volunteer Management System*

## 3.4 **Communications Interfaces**
- **CI-1:** The Volunteer Management System shall send a text message or email (depending on user settings) to the volunteer when they have been assigned to a case.
- **CI-2:** The Volunteer Management System shall send a text message or email (depending on user settings) to the person who requested a volunteer when a volunteer is coming to assist them.

# 4. **System Features**
![](https://github.com/mnolander/volunteerMS-SRS/blob/main/FeatureTree.png?raw=true)

*Feature tree for Volunteer Management System*

# 5. **Other Nonfunctional Requirements**
## 5.1 **Performance Requirements**
- **PER-1:** In the first year, the system should track 60% of the senior cases in the city. 
- **PER-2:** In the first year, the system should provide support to 85% of the reported cases. 
- **PER-3:** The system should also reduce the amount of time it takes to process the volunteers through background checks and other administrative duties.

## 5.2 **Safety Requirements**
- **SAF-1:** Every verified volunteer must undergo a background check following local police regulations before being added to the system.

## 5.3 **Security Requirements**
- **SEC-1:** The personal information of both the volunteers and the people in need of assistance should be kept confidential
- **SEC-2:** The information that goes through the police to do the background checks should not be compromised.
- **SEC-3:** No volunteer who has not been through the background checks should get access to volunteer requests.

## 5.4 **Software Quality Attributes**
- **Interoperability** - The Volunteer Management System shall work with the Background Check System.
- **Security** - Student and Senior Personal Data shall not be shown to volunteers unless they’re selected for the volunteer job.
- **Durability** - The Volunteer Management System shall keep volunteer activity data for two (2) years.
- **Accessibility** - The Volunteer Management System shall be easy enough for seniors to use.

## 5.5 **Business Rules**
- **BUR-1:** An Increase in people applying to become a volunteer / An Increase in available volunteers
- **BUR-2:** Reduced complexity of application/approval process 
- **BUR-3:** Reduction in time for a volunteer to be assigned to a volunteer request 

# 6. **Other Requirements**
No other requirements have been identified for the Volunteer Management System.


# **Appendix A: Glossary**

|**Term**|**Definition**|
| :- | :- |
|VMS|Volunteer Management System|
|SPCC|Senior People Care Center|
|Case|Assistance request assigned to one volunteer|

# **Appendix B: Analysis Models**

![](https://github.com/mnolander/volunteerMS-SRS/blob/main/ERD.png?raw=true)

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

# **Appendix C: To Be Determined List**

There are no TBD references remaining for this document.
