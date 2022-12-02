# **Vision and Scope Document for Volunteer Managment System**
Version 2.0 approved

Prepared by  
Desmond Mack
Michael Nolander
Chris Coulthard

September 23, 2022

|**Table of Contents**|
|:-|
|Table of Contents|
|Revision History|
| Business Requirements|
|Background|
| Business Opportunity |
| Business Objectives and Success Criteria|
|Customer or Market Needs |
| Business Risks |
|Vision of the Solution |
| Vision Statement |
|Major Features |
|Assumptions and Dependencies |
|Scope and Limitations |
|Scope of Initial Release |
|Scope of Subsequent Releases |
| Limitations and Exclusions |
|Business Context |
|Stakeholder Profiles |
|Project Priorities |
|Operating Environment|

**Revision History**

| **Name** | **Date** | **Reason For Changes** | **Version** |
| --- | --- | --- | --- |
| First version | 21/09/22 | Document Created | 1.0 |
| Final version | 23/09/22 | Finished Sections, Polished Document | 2.0 |

# **Business Requirements**

## **Background**

In the past decade or so there has been an ongoing struggle to find health care professionals and care aids as well as the increased elderly population not all being able to afford the services. So in response to this people have started to volunteer for these duties and in this town the local government has taken it upon themselves to facilitate the volunteers. With taking on these extra duties it has put an additional load on the local administration thus being overworked it is taking a long time to match up the seniors in need of help with the volunteers in a timely manner. This is where our system will come in to take the load off of administration and speed up the entire process.

## **Business Opportunity**

This system will provide a service that will connect seniors who need help around the house with volunteers in a much faster manner than the current system which is all done by hand. As well, it will automatically provide background checks so that want to be volunteers can start in approximately 3 days opposed to the current ten days. This system will also have the ability to be expanded so that students can connect to additional tutors outside of their online program.

## **Business Objectives and Success Criteria**

The city and mayor set out to make a system that would replace the current outdated, and less efficient system. The system would make it easier for people to apply to become a volunteer, and for School and Seniors to request a volunteer faster. Measurable criteria to see whether the new system is successful includes:

- An Increase in people applying to become a volunteer / An Increase in available volunteers
- Reduced complexity of application/approval process
- Reduction in time for a volunteer to be assigned to a volunteer request

## **Customer or Market Needs**

There are two primary types of customers: one of which puts out a request for volunteer services, and the other that will search and fulfil those requests. Currently they are having an issue getting volunteers approved quickly due to criminal record checks taking a very long time.
 Below are the primary metrics that we will be targeting in our system.

- In the first year, the system should track 60% of the senior cases in the city.
- In the first year, the system should provide support to 85% of the reported cases.
- The system should also reduce the amount of time it takes to process the volunteers through background checks and other administrative duties.

## **Business Risks**

One of the main risks for the volunteer system is in regards to properly certifying a new volunteer. Adding a dangerous or unfit individual to the volunteer list is a high risk that can result in risk for anyone submitting a case. The main action taken to mitigate this risk is to partner with the police department to utilise their background check system to ensure every volunteer is a good fit for the system. We believe this will increase user acceptance in the city. Otherwise, there are no existing solutions that will compete with this system.

# **Vision of the Solution**

## **Vision Statement**

Our company seeks to provide an efficient and straightforward way that will connect senior aid volunteers to those who are in need of the service. This service should streamline the application process for those in the city providing administrative duties and have the capacity to later be used for other volunteer opportunities.

## **Major Features**

1. **Case requesting** : Allows anyone in need of a volunteer to submit a case into the system. This also includes a notification system to alert the volunteer organization when a new case is submitted, as well as the ability to edit and close currently open cases.
2. **Case history** : All cases, open and closed, are stored in the system in which the volunteer organization can generate a case report to obtain a summary of the number of active cases and detailed statistics. The system displays a list of all currently active cases and archives all closed cases, which allows the organization to view old case details anytime after it has been closed.

## **Assumptions and Dependencies**

Assumptions

- It is estimated around 10,000 to 15,000 senior cases that need help in the city.
- The crime rate in the city is expected to eventually increase by 10% in business transactions in local shops and the Downton area.

Dependencies

- Automatic police certificate check system, system depends on this as every volunteer needs to complete a check using the system.
- Online teaching services used by students, which is an alternative to the volunteer system which can reduce the load on the new system.

#


# **Scope and Limitations**

## **Scope of Initial Release**

Our system will be providing an automated background check and a system that allows requests to be put in for volunteer work and then to match those to volunteers. Individuals looking for volunteers will put in a request detailing what they need to be done and when as well as contact information. Then people with matching skills or abilities can confirm and meet those requests.

![](RackMultipart20221202-1-tijd6q_html_cbb2bc51c8373ac1.jpg)

## **Scope of Subsequent Releases**

- First Subsequent Release: Polish any user submitted issues
- Second Subsequent Release: Multi-language support
- Third Subsequent Release: Mobile Application (iOS/Android)

## **Limitations and Exclusions**

Some advanced features, such as viewing archived cases, may not appear on the initial release but will be added in future releases. Another limitation in this release could occur when a volunteer is assigned a case but does not accept it, which could cause a delay in the case submitter receiving help.

# **Business Context**

## **Stakeholder Profiles**

| **Stakeholder**  |  **Major Value**  | **Attitudes**  | **Major Interests**  |**Constraints** |
| --- | --- | --- | --- | --- |
| City | Increased number of volunteers | Reduce volunteer assignment time by 30% | Would provide a faster and easier system for people to apply to be a volunteer, or to request volunteers | System can process requests within 48 hours |
| Volunteers | Easier to apply | Receptive as they can receive promotions from local businesses | Automatic criminal record check, fast and simple process to apply
| Schools | Easier and Faster to request multiple volunteers | Very receptive: Would provide possibilities for extra tutoring and coaching for students | Ability to request volunteers faster |
| Seniors | Easier and Faster to request a volunteer | Receptive: Could get help faster | Ability to request a volunteer quicker |
 |

## **Project Priorities**

| **Dimension**  | **Driver (state objective)** | **Constraint(state limits)** | **Degree of Freedom (state allowable range)** |
| --- | --- | --- | --- |
| Schedule | Release 1.0 available by end of November 2022 | Release must happen before end of year | Can delay project by up to 2 months, given it is released before end of year |
| Features | Include case tracking and case request features | Initial release must contain basic version of features, with more advanced aspects to be added in future versions | Basic features and 70% of advanced features must be implemented by end of year |
| Quality | Limit the number of user error reports | Must have less than 20 user error reports in the first 3 months of release | 90% of user acceptance tests must pass with Release 1.0 |
| Staff | Have a team with the smallest size possible without negatively affecting the system | Maximum team size is 20 people (not including volunteers) | 30% of staff may be on leave at one time |
| Cost | Minimize costs as much as possible | Maximum budget of $1,000,000 | Budget may be overrun by 10% of maximum |

## **Operating Environment**

The user base will be in a centralised location, as it will serve people living in the city where it is being operated. Users will access the system from various locations around the city, as well as potentially some smaller communities outside of the city. Anyone who is in need of a volunteer will submit a case using the online portal. All volunteer information, case data, and case history will be stored on a cloud solution. There are no concerns regarding response times to access data because there will not be any urgent need for data stored in the system, as well as the fact that most delays in the system will come in the form of waiting times on dependent systems, such as the police background check. General security protocols for cloud data will be enforced, such as encryption. Service interruptions are possible in the case of maintenance, but these events will be timed to minimise user impact.
