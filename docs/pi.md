# Informatics Project

## **Project Proposal**
* [A Digital Signage System for DETI](files/Project_Proposal.pdf)

## **Inception Phase**
* [M1: Inception Phase Presentation](files/M1_Presentation.pdf)

### **Context**
As technology evolves, so does our mode of communication. In the past, a simple piece of paper with a few words could effectively convey an idea. However, in today's fast-paced environment, things change rapidly. Ideas evolve, new developments arise, and the need to reach millions of people simultaneously may arise. Traditional signage is no longer the most efficient method of disseminating information; this is where digital signage steps in.

No longer do we need to manually update room schedules or leave a paper notice indicating an ongoing meeting. No more basic videos with manual set up required. Digital signage handles these tasks seamlessly.

### **Problem**
#### **Integration with the university’s IDP**
Incorporating university's IDP in our software is a key requirement for the final product. While implementing login based on the university's IDP might appear straightforward, it is likely to pose complexities given our unfamiliarity with this field. Moreover, such integration typically involves a time-consuming acceptance process, adding to its difficulty.
#### **Test driven development implementation**
To mitigate future errors and ensure a seamless software development process, we will implement tests for our backend. These tests will be integrated into GitHub Actions, allowing us to identify errors before they are committed to more critical branches, thus enhancing the reliability of our codebase.
#### **User friendly Content Creation Tool (CCT)**
Designing a user-friendly interface is a complex endeavor. Developing user-friendly software presents an even greater challenge, as it necessitates concealing numerous complex operations. Crafting a user-friendly interface and software that empowers users to create their own templates will undoubtedly be a formidable task.
#### **Good documentation and installation guides**
Given that this project is intended for continuous development and enhancement over the years, it is imperative to establish comprehensive and dedicated documentation, including clear guidelines for both usage and installation.
#### **Scalability and Performance**
At the outset, we will operate with only a few computers, rendering scalability and performance less pressing concerns. Nevertheless, considering the ultimate goal of deploying this project university-wide, it is crucial to anticipate and strategize the design and development of our system in a scalable manner without sacrificing performance or necessitating an excessively powerful server.

### **Goals**
#### **Manage electronic displays remotely.**
Our system must be a centralized system with distributed components.

- Centralized System: The main server with the database and software acts as a central hub where data is stored and processed. This centralization provides a single point of control and management for the system.

- Distributed Components: Information is transmitted to Raspberry Pis via the network, facilitated by a broker. These Raspberry Pis function as endpoints, receiving and requesting data from the central server. They are capable of performing additional processing or executing actions based on the received information.
#### **Have a Media Player that allows for displaying content and receive real time updates from different sources.**
We are required to implement a Media Player capable of seamlessly displaying content and receiving real-time updates from diverse sources.
#### **Have a Content Management System to manage all the screens and allow scheduling and timing of content playback.**
Develop a robust Content Management System (CMS) empowering administrators to monitor screen statuses and logs, while providing users with the capability to schedule content playback at specific times and chosen templates.
#### **Create a Content Creation Tool that assists the users designing the templates.**
As mentioned earlier, we require user-friendly software that effortlessly provides all the necessary tools for creating and manipulating templates.

### **Expected Results**
#### **Minimal Viable Product (MVP) of a Digital Signage System**
The functionalities that are expected from us are a software that allow for monitoring, adding, manipulating and configure display of monitors. IDP integration and CCT is a challenge, but doable ones.
#### **User-friendly Content Management System (CMS) and Content Creation Tool (CCT)**
Both a user-friendly CMS and CCT is expected from us by the end of the project. These tools have to be built in a way that provide scalability and easy understanding.
#### **Integration with the university’s IDP**
Our project requires login to be based on university's IDP.
#### **OS image that auto-boots into the Media Player upon startup**
We need an OS image programmed to boot our software automatically, initiating communication with our backend upon network connection.
#### **All the code should include tests and comments**
Every piece of code must be accompanied by thorough testing suites and if a function's name lacks clarity, ensure comprehensive testing and comments are provided to elucidate its purpose and functionality.
#### **Clear documentation and contribution guidelines**
Due to its open-source nature, ensure transparent and accessible documentation along with contribution guidelines, allowing next students or professionals to have an easy time to build upon our software.

### **Task list**
- Raspberry pi configuration
- Template design/requirements
- Architecture development / System design and planning
- Content Distribution Strategy
- Communication plan (documentation)
- Tests (User acceptance and System)
- User friendly CCT

### **Calendar**
Our initial calendar can be found in our M1 presentation; however, it provided only a broad overview of the problem. Therefore, we do not consider it as the definitive calendar. Instead, the following [Calendar](files/calendar.png) is more reliable.

### Templates
* [Media Player Display](https://www.figma.com/file/nFPoHZyNCIRHpyrcfsxKiu/Media-Player-Templates)


## Elaboration Phase
* [M2: Elaboration Phase Presentation](files/M2_Presentation.pdf)

### Comunication Plan

The following table summarizes the recommended communication channel based on the purpose of communication:

| Purpose | Channel |
|---|---------|
| Real-time discussions, quick updates, task delegation and informal communication. | Discord |
| Formal communication, and information sharing. | Outlook |
| Code collaboration, version control, and issue tracking. | Github  |

**Detailed Use Cases**

* **Discord** <img src="../files/iconsHome/discord.png" width="30px" align="top">
	* **Use Cases:**
		* Team discussions for brainstorming, project updates, and ad-hoc questions.
      	* Assigning tasks and tracking progress.
		* Sharing quick wins, announcements, and real-time project status updates.
* **Outlook** <img src="../files/iconsHome/outlook.png" width="45px" align="top">
	* **Use Cases:**
		* Sending official emails, meeting information, and project reports.
* **Github** <img src="../files/iconsHome/github.png" width="30px" align="top">
	* **Use Cases:**
		* Hosting code repositories, managing changes, and tracking development progress.
		* Reporting bugs, requesting features, and collaborating on code solutions.
		* Maintaining a central location for project files and documentation.

### **Organization**
[UA Smart Signage](https://github.com/UA-Smart-Signage-Platform)

**Repositories**

- [Documentation Website](https://github.com/UA-Smart-Signage-Platform/Documentation-Website)
- [Content Manager System and Content Creator Tool](https://github.com/UA-Smart-Signage-Platform/Content-Manager-System-and-Content-Creator-Tool)
- [Media Player](https://github.com/UA-Smart-Signage-Platform/Media-Player)
### **Context and State of The Art (SOA)**
In the context of digital signage Aveiro University (UA) has been using static display for videos and information in televisions across all monitors within the Department of Eletronics, Telecommunications and Informatics (DETI). No prior software has been developed in this regard within UA.

To display videos, DETI is currently using a Media Player on a windows machine to display them. Due to its limitations we are building a software from the ground with a flexible structure, schedule functionality and dynamic information display.

The project aims to build a system that will be used over the years and done in a way that can be improved and built on easily.

### **Functional Requirements**
**Content Management**:

- Ability to upload, manage and organize content.
- Support for various media formats (images, videos, text).
- Content scheduling for specific times or events.

**Display Management**:

- Control over which screens display specific content.
- Grouping of screens.
- Support for remote display management and configuration.

**Integration**:

- Integration with external data sources (RSS feeds, social media, APIs) for dynamic content.
- Compatibility with various screen types.

**User Interface**:

- Intuitive user interface for content management.
- Role-based access control for different users (administrators, content managers, etc.).
- Reporting and analytics features to track content performance and screen status.


### **Non-Functional Requirements**
**Performance**:

- Fast response times for content uploads and updates.
- Smooth playback without buffering or lag.
- Scalability to support a growing number of screens and users.

**Reliability**:

- High availability to ensure screens are always operational.
- Fault tolerance to handle hardware failures or network issues.
- Disaster recovery capabilities to recover from system failures (backups).

**Security**:

- User authentication and authorization mechanisms.
- Encryption of data during transmission and storage.
- Protection against unauthorized access and tampering of content.

**Scalability**:

- Ability to scale the system as the number of screens or content volume increases.

**Usability**:

- Support for localization.

**Compatibility**:

- Compatibility with various operating systems and web browsers (raspi by construction should be always the same, react should be universal).
- Compliance with industry standards and protocols (HTML5 + RESTful APIs).

### **Personas**

**Nuno - DETI Director**

- Name: Nuno
- Age: 37
- Occupation: Technician

Background:

- Seasoned university employee with over 15 years of experience.
- Recognized for administrative excellence and valued by colleagues.
- Limited experience with design aspects.
- Prefers user-friendly and straightforward technological platforms.

Goals:

- Effortlessly share pre-made content, including:
	- News announcements
	- Promotional videos
	- Other relevant resources
- Manage the displayed information through a simple and intuitive interface (add/remove screens).

*Note: Nuno's technical expertise lies primarily in administrative tasks. Aim to provide clear and concise instructions for content management.*

**Sara - UI/UX Designer**

- Name: Sara
- Age: 30
- Occupation: Designer


Profile:

- Software: Prefers feature-rich and customizable tools to unleash her creative potential.
- Workflow: Values efficient tools that streamline design processes and enable quick production of high-quality content.
- Design Approach: Enjoys experimentation with various design elements and actively seeks new features and functionalities.

Goals:

- Create engaging content specifically designed for display on DETI screens.
- Utilize her creativity to design unique templates for showcasing on designated displays.


**Rodrigo - DETI Student**

- Name: Rodrigo
- Age: 19

Background:

- Enthusiastic and curious student with a thirst for new knowledge and experiences.
- Actively seeks out relevant information related to academics, cultural events, and networking opportunities.

Goals:

- Easy and swift access to crucial information concerning:
	- Coursework
	- Academic events
	- Extracurricular activities
- Clear and organized presentation of information for staying updated on the go.


### **Use Cases**
![Use Cases](./files/useCasesDiag.png)


### **User Stories**

#### As an administrator:
- **Edit Template Content:** I want to edit template content so that I can keep it up-to-date.
- **Schedule Content:** I want to schedule specific content on digital screens at designated times and dates so that I can effectively manage content dissemination.
- **Delete Templates:** I want to delete templates so that I can remove outdated or unused content.
- **Edit Groups of Screens:** I want to edit groups of screens so that I can update the organization of presentations.

#### As a designer:
- **Create Templates:** I want to create templates so that I can define the structure and content of presentations.
- **Choose Widgets:** I want to choose widgets for the template so that I can add interactive elements to presentations.

#### As a viewer:
- **View Screens:** I want to see screens so that I can stay updated with the latest content.
- **View Scheduled Content:** I want to view content scheduled for specific times or dates so that I know what information is available when.

### **Templates**
- [Content Management System / Content Creator Tool](https://www.figma.com/file/y6D627skVNvPySSFYa8zkI/CMS-%2F-CCT-Templates)
- [Documentation Website](https://www.figma.com/file/OYqGSLiljrJLuEHH0NNRfO/Documentation-Templates)

// TODO (Add certain topics related to M2, refine user stories)

### System Architecture



## **Checkpoint 1**
- [Checkpoint 1 Presentation](files/Checkpoint1_Presentation.pdf)

// TODO (Add user flow, etc.)

### Frontend

**What is done**

- Design of pages on figma
- Static UI
- Local SonarQube
- Docker configuration

**What wiil be done**

- Incorporate backend integration logic by coding the functionality to make calls to backend endpoints.
//TODO

**Problems**
// TODO

### Backend

**What is done**

- Local SonarQube
- Docker configuration
- Endpoints for the modeled entities
- Some tests for the entity monitor
- Mosquitto configuration and comunication with media player
- Mock data 
- Tweaks to database and architecture models


**What will we do**

- Tests for the rest of the entities and endpoints
- Improvements to some backend logic
- InfluxDB configuration

**Problems**

- Constant changing of database model
- Some logic missing

### Media Player

**What is done**

- Logging
- Message protocol
- Mosquitto configuration and comunication with backend
- API implementation
- HTML generator mockup

**What wiil we do**
//TODO


**Problems**
//TODO


###	User Workflow




## **Prototype Phase**
- [M3: Prototype Phase Presentation]

// TODO

## **Last Phase**
- [...]

// TODO

---

## **Sprints**
### 01/03/2024 - 08/03/2024
**Summary**

```
- Create github organization (and add tutors to it)
- Add tutors to discord and create respective channels
- Start working on documentation
- Research about different real life examples (in practice)
- Organize group into sub-groups
- Document with link to the website
- Create and propose architecture 
- Requirements gathering, both functional and non-functional and personas with scenarios.
- Create calendar
- Figma
- MP mockup
```

**Detailed version**

`As this was the first week, we did not think about providing a detailed report.`

**Sprint results**

`All items were completed within time.`

---

### 09/03/2024 - 19/03/2024
**Summary**
```
Frontend
- Create CMS in figma
- Initialize React's basic code
- Docker configuration
- Initialize documentation page

Backend
- Basic endpoints initialization
- Database entities
- Docker configuration

Media Player
- Flask request API
- Mock up of widget converter / setting up format for widgets and templates

Extra
- Create dedicated repos and backlogs
- M2 Presentation
- Domain Model
- User Stories
```
**Detailed version**

```
Frontend

- Create CMS in figma (before client's feedback)
	- Create all pages related to it 
- Finish figma CMS UI (after client's feedback)
	- Added buttons for visibility in some areas (client's request)
	- Created scheduler page
	- Created pending monitors pop up
- Initialize frontend code
	- Started Component side bar
	- Started Component page title
- Initialize React's basic code
- Docker configuration
	- Created docker for react and docker-compose for the entire application (skeleton only)

Backend

- Docker configuration
	- Created docker and docker-compose for spring boot
	- Created docker for databases (currently missing env file to change password and db name)
- Created Spring models
	- File and content in progress
	- Currently missing user model
- Created basic Endpoints functionality
- Created some Tests
	- Screen and monitor group are done
	- Template in progress

Media Player

- Basic Implementation of MQTT client
- Started Logging
- Proof of Concept of Playing Multiple Videos (playlist)
- Mockup of HTML Generator from Template

Extra

- Tweak architecture
	- Removed unnecessary database (mongoDB)
	- Small tweaks have been done to match our needs
- User flow diagram
	- Created flow diagrams for both users (Admin and User)
- Start report
	- Report's initial skeleton is done
- Create database model
- Created user stories
- Initialize documentation page
	- Customized landing page
	- Create documentation page structure
	- Added information to documentation
	- Added basic guidelines
	- Added information to PI tab
- Created dedicated repositories and backlogs
- Created M2 Presentation
```


**Sprint results**

`All items were completed within time.`

---

### 20/03/2024 - 26/03/2024
**Summary**

```
Frontend
- Create side bar component
- Create header component
- Create group menu component
- Create static monitors page
- Create static specific monitor page
- Create static media page

Backend
- Research and start working on broker
- Fix docker compose
- Data initialization (mock)
- Endpoints
	- Fix some errors
	- Create missing tests

Media Player
- Research about OS image and daemons
- Research and start working on mosquitto (broker - alongside backend)
- Started set up message protocol
- Research about news API

Extra
- Add SonarQube to frontend
- Add SonarQube to backend
- Continue documentation
- Ask for videos
```

**Detailed version**
```
Frontend
- User Interface
	- Created static media page
	- Created static dashboard page
	- Created static monitors page
	- Created static specific monitor page
	- Created various components
- Testing
	- Added local Sonarqube to verify frontend code smells and alike

Backend
- Integrated MQTT (server-docker connection)
- Inserted dummy data for testing (files, monitors and monitors groups)
- Created endpoints to upload files and folders
- Minor adjustments to models
- Testing
	- Created unit tests for services/repositories
	- Created integration tests for controllers

Media Player
- Research and Implementation of news API
- Figuring out how to create OS image
- Improved implementation of MQTT client
- Started implementation of message protocol

Extra
- Tweak architecture
	- Added influxDB for logging and monitor status
- Tweaked database model
- Updated documentation
```

**Sprint results**

`All items were completed within time.`

---
### 27/03/2024 - 02/04/2024

`- No sprint was set for this week due to holidays and other subject works.`

---

### 03/04/2024 - 09/04/2024
```
Frontend
- Make pages dynamic
- Design login
- Research Calendar
- Implement login (?)
- Start working on calendar (?)

Backend
- Work on influxDB
- Add swagger
- Add github actions (automatic tests)
- Implement basic log in
- Fix code logic and structure

Media Player
- Backend integration
- Continue Message Protocol
- Work on automatic setup
- Mock schedule

Extra
- Implement sonarcloud for organization (frontend, backend and MP)
- Configure docker compose onto a single main one.
- Decide logs Time To Live (TTL)

Monday (08/04/2024)
- Refactor code
- Work on documentation
- Work on report
```

**Detailed version**
```
TODO
```

**Sprint results**

---