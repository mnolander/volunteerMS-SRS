# User Requirement Document

Chris Coulthard

Michael Nolander

Desmond Mack

October 17, 2022

## 2.1 User Classes

Direct user classes

- **Volunteers** (favoured) - Approved users who have submitted their information into the system and can volunteer for requests. This also includes the student-peers and senior-peers, who get assigned to specific people in need of volunteer work.
- **Volunteer administrators** (favoured) - Users with higher privileges who can approve new volunteers, view volunteer statistics, and assign volunteers to cases.
- **SPCC staff** (favoured) - Employees in the Senior People Care Centre who receive senior people's information and create profiles for them in the Volunteer Management System.
- **School staff** (ignored) - Or school administrators; users who submit requests to the Volunteer Management System on behalf of students.

Indirect user classes

- **Senior people** (favoured) - Users who request volunteer work by calling the SPCC and are assigned a senior-peer.
- **Police officers** (ignored) - Manually approve background checks in the background check system to validate new volunteers.

## 2.2 Potential Actors

- **Volunteer** - Approved users whose information has been submitted into the system and can volunteer for requests.
- **Student-peer -** Volunteer who is assigned to a student to provide teaching assistance.
- **Senior-peer -** Volunteer who is assigned to a senior person to provide assistance, such as reminding them of important dates and record the senior person's health status.
- **Volunteer administrator -** Highly privileged user who can approve new volunteers, view volunteer statistics, and assign volunteers to cases.
- **SPCC staff -** Employee working in the Senior People Care Centre who gets senior people's information over the phone and creates profiles for them in the Volunteer Management System based on the information received.
- **School administrator -** User who submits volunteer requests on behalf of students to get them teaching assistance.
- **Background check system -** Operated by the police department; receives new volunteer information, checks their credentials and history, and approves or denies them based on an officer's final decision. This result is sent back to the Volunteer Management System.
- **Unapproved volunteer -** Any user who has not been approved as volunteers and has not completed a background check; are not allowed to access the system.

## 2.3 Use Cases

| **Use Case** | **Description** | **Involved Actors** |
| --- | --- | --- |
| Submit volunteer information | Volunteer submits their information into the system. | **Primary** : Volunteer **Secondary**: Volunteer administrator |
| Approve new volunteer | Volunteer administrator approves a pending volunteer and accepts them into the system. | **Primary**: Volunteer administrator **Secondary**: Volunteer |
| Create senior person profile | SPCC staff creates a profile template for a senior person and submits it into the system. | **Primary**: SPCC staff **Secondary**: Volunteer administrator |
| Submit teaching assistance request | School administrator submits a request for a student-peer into the system on behalf of a student. | **Primary**: School administrator **Secondary**: Volunteer administrator, student-peer |
| Deny access to system | An unapproved user attempts to access the system, but is denied due to not being in the approved volunteers list. | **Primary**: Unapproved volunteer **Secondary**: Volunteer administrator |
| Send volunteer information | Volunteer information is prepared and sent to the police background check system to validate new volunteer information. | **Primary**: Volunteer administrator **Secondary**: Background check system |
| Assign volunteer to case | Volunteer administrator assigns a volunteer to a case. | **Primary**: Volunteer administrator **Secondary**: Volunteer |
| Send senior person's health status | Senior-peer submits a senior person's health information and status to the system. | **Primary**: Senior-peer **Secondary**: SPCC staff |

## 2.4 Use Case Diagram

![](RackMultipart20221202-1-a5o7d3_html_8453125a006d6095.png)

## 2.5 "Create New Volunteer" Use Case

| **Use Case Section** | **Comment** |
| --- | --- |
| **Use Case Name** | Create New Volunteer |
| **Scope** | Volunteer management system |
| **Level** | The goal is to enter a new volunteer into the system |
| **Primary Actor** | volunteer |
| **Stakeholders and Interests** | Volunteer, Volunteer administrator, police, developer, senior, public |
| **Preconditions** | There needs to be someone who needs to volunteer |
| **Success Guarantee** | The background check must be completed |
| **Main Success Scenario** | Volunteer fills out application and passes background check |
| **Extensions** | Volunteer fails background check |
| **Special Requirements** | Must process request quickly |

## 2.6 "Approve New Volunteer" Use Case

| **Use Case Section** | **Comment** |
| --- | --- |
| **Use Case Name** | Approve New Volunteer |
| **Scope** | Volunteer Management System |
| **Level** | Goal is to approve newly registered volunteers. |
| **Primary Actor** | Volunteer Administrators |
| **Stakeholders and Interests** | Volunteer Administrators, Volunteer, Police, Seniors, Students, Teachers, Parents, Software Developer |
| **Preconditions** | - List of Newly Registered Volunteers 
||- Background Check System is running |
| **Success Guarantee** |
||- Initial Screening complete
||- Background Check complete
||- Education Check complete
| **Main Success Scenario** | Volunteer Registered, All Background Checks are Completed, Administrators Approved Application |
| **Extensions** | Volunteer Fails the Background Check or Education Check (for Student Volunteers) |
| **Special Requirements** | - Background Check System is Working
 |

## 2.7 "Generate Daily Report" Use Case

| **Use Case Section** | **Comment** |
| --- | --- |
| **Use Case Name** | Generate Daily Report |
| **Scope** | Volunteer Management System |
| **Level** | Goal is to Provide the Volunteer Administrators with a Daily Report |
| **Primary Actor** | Volunteer Administrators |
| **Stakeholders and Interests** | Volunteer Administrators, Volunteer, Seniors, Students, Teachers, Parents, Software Developer |
| **Preconditions** | - Volunteers are being requested
| **Success Guarantee** | - Seniors/Teachers are Requesting Volunteers
| **Main Success Scenario** | Administrator Receives Reports Daily and Gets the Next Week's Report Successfully. |
| **Extensions** | Volunteers aren't being requested leading to no data for reports |
| **Special Requirements** | - Daily Reports
||- Algorithm for calculating next week's cases
 |
