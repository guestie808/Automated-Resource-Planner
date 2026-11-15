# Product Initiation Document

## Product Name: Automated Resource Planner

## Project Sponsor: Hazel Jordan - Enterprise Architect

## Project Team: Team 6
- Tyler Guest
- Morgan Jones
- Kyran Boyce
- Will Tuffrey
- Connor Bond-Webber

## Document Control
| Version | Issued | Details of Change | Author |
| --- | --- | --- | --- |
| v0.1 | 23/10/26 | 1.1-1.3 draft | Tyler |
| v0.11 | 26/10/26 | Initial interview questions written | Tyler, Kyran, Will, Morgan |
| v0.12 | 27/10/26 | Mock up designs created for interview | Tyler, Kyran, Will, Morgan, Connor |
| v0.13 | 28/10/26 | Initial meeting with client | Tyler, Kyran, Morgan, Connor |
| v0.14 | 01/11/26 | Interview transcript processed, summarised | Tyler |
| v0.15 | 01/11/26 | Expanding 1.1 Purpose section | Connor |
| v0.16 | 01/11/26 | Expanding 1.3 Approach | Will |
| v0.17.0 | 08/11/26 | 2.1-2.3 Draft | Connor |
| v0.17.1 | 08/11/26 | Expansion of the section 2.3 draft (excluding a proper expansion of "Costs") | Will |
| v0.18 | 09/11/26 | 1.4 Completed and 2.3 Feedback | Tyler |
| v0.19 | 09/11/26 | 1.2 Completed | Kyran |
| v0.20 | 15/11/26 | 2.3 Completed | Morgan |
| v0.21 | 15/11/26 | 2.3 Tidied up | Will |


## Document Particulars
**Review & Sign-Off**

**Authors (Responsible)**

| Name | Contribution |
| --- | --- |
| | |

**Approvers (Accountable)**

| Name | Sign-Off Date |
| --- | --- |
| | |

**Support (Supportive)**

| Name | Contribution |
| --- | --- |
| | |

**Reviewers (Consulted)**

| Name | Level of Review/ Criteria |
| --- | --- |
| | |

**Distribution (Informed)**

| Name | Role |
| --- | --- |
| | |

## Contents
- [**1 Project Definition**](#1-project-definition)
  - 1.1 Purpose
  - 1.2 Aims & Objectives
  - 1.3 Approach
  - 1.4 Success Criteria
- [**2 Business Case**](#2-business-case)
  - 2.1 Background
  - 2.2 Options Considered
  - 2.3 Benefits, Costs and Constraints
- [**3 Project Scope**](#3-project-scope)
  - 3.1 Scope - Inclusions and Exclusions
  - 3.2 Deliverables
  - 3.3 Risks
  - 3.4 Assumptions
  - 3.5 Issues
  - 3.6 Dependencies
- [**4 Communications and Stakeholders**](#4-communications-and-stakeholders)
  - 4.1 Reporting
  - 4.2 Project Team Membership and Roles
- [**5 Conclusion**](#5-conclusion)
- [**6 Appendices**](#6-appendices)

## 1 Project Definition
### 1.1 Purpose
The purpose of this project is to develop an automated resource planner to improve and replace the current manual process of scheduling practical sessions. The new system will aim to reduce time and effort required for staff to organise sessions by automating the allocation of rooms, equipment and technicians using timetable data imported from CSV files.

This new system will check the timetable data and match each practical sessions with the needed resources that is also based on availability, for example allocating the appropriate room based on things like the required equipment for the students and the technician needed for the room.

Another key feature is a way of managing and distributing any updates or relevant information to the students, technician, equipment and room calendars.

The system should also prioritise ease of use, providing a clear and straightforward interface that allows staff to import timetables, review generated schedules and manage resource allocations in a simple and accessible way for all staff members.

Finally the project may include a system to avoid, scheduling conflicts, like rooms being double booked, not having the right equipment or a technician not being able to set up the equipment due to being spread across too many sessions. This will help ensure the system produces reliable and accurate sessions, especially if multiple people are using this system 

### 1.2 Aims & Objectives
*Define the goals, long-term outcomes, and the objectives, short-term outcomes, of the project. Make sure objectives are SMART and link back to the purpose.*

Long Term aims/goals:
- To develop a fully functional & autonomous windows application capable of assigning vacant rooms and appropriate technicians with minimal manual intervention from the client when provided with a CSV file.
- To implement direct integration for Microsoft azure systems. Allowing the automation of updates to student, technician and room timetables directly, further decreasing the manual intervention required.
- To design the software with expansion in mind to allow adaptations in the future to support more departments across the university.

Short Term
  - To create various draft designs to work out an appropriate Windows UI that'll be extremely user-friendly. Interviews with the client will be held to work out usability and efficiency.
  - Developing a system that'll read CSV's with little to no error, using black & white box testing, extracting and sorting all the information regarding students, class dates and requirements.
  - Coding an early build that could test the systems output using .ICS files , creating invites that will prove output functionality.

### 1.3 Approach
We will use an Agile oriented approach for ensuring the goals of this project are met on time and to a good standard of work. This method allows for regular checks with the client to make sure their requests are met.
Using the Scrum agile framework with sprints is a great way to ensure this.

Regular and frequent communication with the client is vital to gain feedback on each iteration of the project. We aim to email the client regularly (weekly/biweekly, timescale to be determined within the next week) and try to have a meeting (online or in person) in necessary intervals to give comprehensive updates on progress and try to incorporate the client’s own ideas which they may have in relation to the work committed since the last update.

Each member of the team will have their own specific roles for this project (Project Manager etc, for example). On top of this, the work for the project will by default be split for everyone to do as a collective. How much of this will depend on what other role specific tasks each person is undergoing at the time.

### 1.4 Success Criteria
- 100% of valid CSV files to be recognised and processed
- 100% of invalid CSV files to be handled with a suitable error
- 75% of rooms, equipment, and technicians to be assigned automatically, without human intervention
- 100% of overlapping schedules to be brought to attention of the user to be amended
- 100% of technician accolation to be within the defined vicinity rules
- 100% of exported schedules to appear in Outlook Events to be sent of to necessary recipients
- 100% of exported events to contain all required information/ supporting documentation
- Reduce schedule processing time by atleast 50%
- System to be fully tested, evaluated, and implemented by 21st April 2027
- System should be suitable to be adapted to additional courses in the future
- System should receive atleast a 75% satisfaction rate compared to previous system

## 2 Business Case
*The business case is the document that justifies the project. It’s similar to what’s discussed in the project definition but goes into greater detail.* 
### 2.1 Background
The Current system for scheduling healthcare practical teaching sessions is done by staff manually importing timetable information using CSV files into Microsoft Outlook. The staff then have to allocate suitable rooms, equipment and technicians for each session one at a time. Finally distributing the sessions and their information to students and staff. This process is not very efficient due to the amount of manual effort and time needed to set up these sessions, especially as there are multiple everyday spread across the different courses.

This also leads to the possibility of scheduling and user errors, things like rooms being double booked, allocation of unsuitable or unavailable equipment.

#### From Connor For next person 
- please do Include one or more relevant Business Analysis techniques from IT Practice: Skills, Models, and Methods. At the moment I'm thinking of SWOT analysis in a table or in separate paragraphs to identify 
- Strengths: What works well in the existing system? 
- Weaknesses: What problems exist?
- Opportunities: What could be improved?
- Threats: What could prevent improvements from succeeding?
- Please then talk about why you used your method of business analysis

#### Questions for 2.1
- ask our tutor which she would prefer and if she would be happy with us using SWOT*
- Ask what opinions are on what we've got and what can be improved
- does she want a paragraph in this about what the new system aims to do 

### 2.2 Options Considered
Option 1 -Continue using existing manual process (Talk about how it would be a familiar system, but would not address the problem of this brief)

Option 2 - Use a spreadsheet based application (talk how it could be more structured but still require manual effort)

Option 3 - Looking at our rough designs talk about how we have considered different approaches of design, like using a weekly calendar, a monthly one etc

Other options that we can think of to add to this will help

*Include one or more relevant Business Analysis techniques from IT Practice: Skills, Models, and Methods.* 

There are several possible solutions that can be considered to address the manual process of scheduling practical teaching sessions. Each option is evaluated based on its ability to reduce the manual load, improve the resource allocation, reducing or nullifying scheduling conflicts and to make a prototype and integrate it with the university's existing systems.

Option 1 is to continue using the existing manual process where the staff will import the csv files into Microsoft outlook and manually allocate rooms ,technicians, equipment and supporting documentation. The advantage of this approach is staff are already familiar with this system and staff wont need any training or changes to their current work processes. It would also cut out the costs of having to make a new system. However this would not address the project brief. This process is time consuming and increases the possibility of human error, as exam season comes to a start this means that the process would be come difficult to manage. Continuing with this process would be the simple short term option but would not improve efficiency.

option 2 would be to develop a spreadsheet based application using Microsoft excel. This could include several worksheets for teaching sessions, room availability and technician availability.
this would have features such as dropdown lists, conditional formatting and formulas would help staff organise information more consistently and identify scheduling conflicts. For example, conditional formatting would highlight sessions where a room or technician has already been allocated. The advantage of this is that Microsoft excel is already widely used and is an inexpensive solution. It would bring more structure into the process compared to the manual approach. However, this would still rely heavily on manually entering information, checking the availability and manually allocating resources. However some tasks can be simplified using formulae and automation. But it would be difficult difficult to complete the automation that is required by the brief. There can also be limitations when multiple members of staff need access to the sheet and all of them are updating information at the same time. The spreadsheet application could provide a useful straight away improvement but would not fully resolve the issue.

option 3 would be to use a different calendar based application. During the initial design stage, there are multiple different approaches to presenting and managing the schedule that we considered. These included weekly and monthly calendar layouts. A weekly calendar would provide a more detailed way of practical teaching sessions, this would prove useful for to identify which rooms, technicians and equipment are being used on particular days. This would be useful to identify busy periods, resource planning requirements in advance and understanding the distribution of practical's throughout the week. Alternatively, a monthly  calendar could provide a broader overview of teaching sessions coming up. This would be useful for once again identifying busy periods, resource planning and understanding the distributions of practical sessions throughout a month.
Rather than these being separate systems, they would both be incorporated into one application with different views. This would allow staff to swap between weekly and monthly depending on their requirements.

Option 4 is to develop a fully automated resource planning system (ARP),  this would directly address the requirements outlined in the project brief and our client meeting.  This system would import the timetable csv and automatically process the teaching sessions which it would compare the requirements of each section against availability of rooms, equipment and technicians before allocating necessary resources, any interventions will be sent to the relevant staff for them to sort out. This would then be sent by email to the technicians, students and course staff with an invite which will put these on the calendars for said people. A really important advantage of this approach is that it addresses the problems with the current approach by reducing manual intervention and it would help prevent double bookings, improve resource utilisation and provide a more consistent scheduling process. This application could also use the calendar layouts mentioned in option 3 allowing users to view the schedule in different formats.

Business analysis 

options appraisal involves identifying and comparing solutions against the requirements and objectives of a project. This approach would be used to consider the advantages, disadvantages and suitability of each option. For this project the evaluation criteria include: the level of automation provided, the amount of manual work required from staff, the ability to identify and prevent resource conflicts, integration with microsoft Outlook, development complexity and cost and the ease of staff and stakeholders.

Stakeholder analysis is relevant because the proposed system would affect staff, technician and students. Each group has different requirements, for example staff need an efficient  way to allocate resources, technicians need accurate information about their assigned sessions and students need reliable calendar appointments containing the correct session details. Considering a stakeholder analysis helps ensure that the solution that is chosen will address the needs of the people who will interact with the system rather than taking more of a hold on its functionality. 

Process modelling would be used to understand the existing process and identify improvements by looking at the current workload it makes it possible to identify tasks that are repetitive and time consuming and venerable to human error. The existing process will be compared with a automated process to demonstrate how importing timetable information, checking resource availability, allocating resources and generating appointments could be handled more efficiently. 

In conclusion after considering and looking at the different options. Option 4 appears to be the best approach for making sure that the requirements of the project are met. However it would require more development effort at the start. The automated resource planner system would provide the best opportunity to reduce manual scheduling tasks and improve the output of rooms equipment and technitions.  


### 2.3 Benefits, Costs and Constraints

#### Benefits
- The software will greatly reduce the workload on the admin. Tasks like these which can be done with automation will always save time in the long run
  * The admin will still be able to use manual intervention where necessary, this intervention won't be nearly the work they would have to commit to before
- One of the major benefits of using an algorithm to make a timetable rather than doing it by hand, is it can reduce the likelihood of a double-booking/conflict. We aim with this project to improve the scheduling efficiency of the timetable system
- Improved efficiency for the staff and students
  * If there happened to be an unexpected reason why the current timetable doesn't work, creating a new one wont take long or stress the course leaders out
- Easier management of multiple teaching sessions
- Potential for future expansions to other courses
  * Theres no reason why this can't be expanded to fit/crossover with other modules or courses taking the same modules

#### Costs
- Time required for designing, devolping, testing, debugging, maintenance and updates of the software
- Time required to train staff to use the software
- Time spent setting up required databases
- Temporary reduction in productivity while staff become familiar with the system
- Computer hardware requirements
- Any licences used in the making of the project - TBC!

#### Constraints
- The project itself is constrained by the available time for development
  * This aspect is dictated by group team effort/allocation and the consistency of the communication from the client
- Requirements established by client and the project itself
  * Implimentation of new features which the client may want to add later on down the line of production
  * Unseen issues regarding the implimentation of the code
  * A sudden lack of communication could lead to certain aspects not getting the time and work the deserve
- Time spent making user guides, documentation and demonstrations



## 3 Project Scope
*Project scope defines the goals, constraints, workflow management, strategies, tasks and deliverables of the project. Again, while some of this is touched upon in the project definition section, this is a more comprehensive account of all the work to be done in the project.*
### 3.1 Scope - Inclusions and Exclusions
*What is included in the scope of the project? What is excluded from the project?* 

### 3.2 Deliverables
*How will the board know that the project has been completed successfully? What products or activities need to be delivered to achieve the project aim and objectives?* 

*Don’t include management deliverables (e.g. PID, report, lessons learned, presentation, Gantt chart), focus on product deliverables. Remember your report must include a section on each deliverable, so don’t add too many.* 
| Deliverable | Lead | Stage |
| --- | --- | --- |
| | | |

### 3.3 Risks
*Identify potential events that may impact the project negatively* 

### 3.4 Assumptions
*What assumptions have been made during the planning of the project?* 

### 3.5 Issues
*Are there any pre-existing issues needing resolution during project execution.* 

### 3.6 Dependencies
*What are the main interdependencies between project deliverables?*

## 4 Communications and Stakeholders
*List the channels of communication the project will be using, what they will be used for and who the intended audience will be.  List the people who will be affected by the work and/or benefits of the project. List anyone else who needs to be kept informed about aspects of the work.*
### 4.1 Reporting
*Detail how project work will be monitored and reported, including how often and to whom.*

### 4.2 Project Team Membership and Roles
*List core team members and their job titles.  Include members of the wider team if helpful.* 
| Name | Role |
| --- | --- |
| | |

## 5 Conclusion
*Include early reflection on progress so far.* 

## 6 Appendices
### Appendix A – Related Documents 

*Here you'll want to create the project schedule, including all tasks, deadlines and milestones, and place them on a timeline (e.g. Gannt chart)*

### Appendix B – Glossary 
