# **Sprints**
To organize what needed doing and alike, sprints were created, along with weekly (friday) meetings with the tutors and a weekly (tuesday) meeting with the group to decide together what needed doing and what each one of us would end up doing.
Every monday a sprint report would be created and delivered to the tutors to keep them up to date.
Structure:
- Summary : TODO list;
- Detailed version : what was done but in detail (might not include everything);
- Sprint result : report if something was missed.

This was supervised/organized by Pedro for most of the project (out of his own free will), however, there were 2 weeks where Pedro put himself on standby so that the team could learn some organizing skills without his help, aiming and providing a way for them to feel the responsability of said position.


## 01/03/2024 - 08/03/2024
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

## 09/03/2024 - 19/03/2024
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

## 20/03/2024 - 26/03/2024
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
## 27/03/2024 - 02/04/2024

`- No sprint was set for this week due to holidays and other subject works.`

---

## 03/04/2024 - 09/04/2024
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
Frontend
- Changed tables in Media, Monitors and Pending Monitors page's to Data Tables
- Started on Media, Monitors and Pending Monitors dynamic information load

Backend
- Started IDP integration (research + tests)
- Added swagger to document endpoints
- Handling of MQTT messages
- Fix some problems related to branch merges

Media Player
- Message Protocol has been defined. Media Player now follows the protocol.
- We were able to establish connection between the media player and the broker inside the same network but different machines.
- Created some tests to allows us to test the register and template parts of the protocol

Extra
- Added and configured Media Player Sonarcloud analysis
- Documentation
 - Added information to Backend
 - Added information to Media Player
 - Added information to PI tab
- Report
 - Added some parts to it
```

**Sprint results**
```
## Missed from sprint ##
Frontend
- Did not fully implement dynamic information loading
- Design login
- Research calendar
- (Not fully decided for this sprint but mentioned)
 - implement login 
 - start working on calendar

Backend
- Work on influxDB
- Add github actions workflow (automatic tests)
- Implement basic log in (substituted with IDP research and tests)
- Fix code logic and structure (some was done but not everything)

Media Player
- Make the media player run when the raspberry pi is booted (will be done tomorrow)

Extra
- Decide logs TTL and structure
- Go over database diagram (will be done tomorrow)
- Go over endpoints and come to a final decision (will be done tomorrow)
- Configure docker compose onto a single file for frontend + backend
- Missing sonarcloud configuration for backend + frontend
- Missing frontend documentation
```

---


## 10/04/2024 - 16/04/2024
```
- No sprint was set for this week besides working for M3 presentation.
```

**Detailed version**
```
N/A
```

**Sprint results**
```
N/A
```

---

## 17/04/2024 - 23/04/2024
```
Frontend
- Make some adjustments to monitors page
- Make some adjustments to media page
- Start working on making dashboard dynamic
- Adding new small UI features to scheduler
- Research/implement calendar (?)

Backend
- Work on influxDB and logs
- Work on UA IDP
- Make some adjustments to Media
- Work on some endpoints/services for dashboard and scheduler

Media Player
- Configure automatic setup on Raspberry PI 5
- Work on fetching media files for templates

Extra
- Decide one-sentence project description
- Elaborate guidelines further

Monday (22/04/2024)
- Refactor code
- Work on technical debt
- Work on documentation
- Work on report
```

**Detailed version**
```
Frontend
- Scheduling menus done(wireframe has been developed which enables users to choose content and set both start and end dates and times) but needs some improvements
- Editing and adding new groups done
- Added breadcrums to the media page

Backend
- Integration tests for monitors and files
- Some tweaks on overall logic for monitorsGroup and tests added
- Final details on schedule entity and respective tests
- InfluxDB working (backend logs added)
- Some tweaks on monitors delete logic
- Some tweaks on overall logic for files and respective tests
- Ua idp working and normal user working

Media Player
- Start with some tests for the implementation of the initial configuration
- Refactor some endpoints to fit with changes in the widgets
- Implemented basic way to download the files sent for the templates

Extra
- Documentation
- Added information to PI tab
```

**Sprint results**
```
Everything seems to have been met.
```

---


## 24/04/2024 - 30/04/2024
```
Frontend
- Implement delete group functionality
- Mock very basic CCT functionality
- Fix update group bug
- Fix schedule rule to send correct information

Backend
- Rework some file service functionalities
- Create more tests overall
- Finish implementing UA IDP login
- Work on sending file download URL to Monitors

Media Player
- Work on more MP configuration

Extra
- N/A

Monday (29/04/2024)
- N/A. Mostly used to finish what's missing from the sprint.
```

**Detailed version**
```
Frontend
- Implemented delete group functionality
- Added resizable divs to CCT
- Fixed bug within update group functionality
- Fixed schedule rule content POST/PUT information
- Finished schedule rule modals

Backend
- Reworked some file service functionalities
- Created more tests
- Unit tests for content, template, widget, templateGroup and templateWidget
- Integration tests with 2 containers for files and monitor
- Finished implementing UA IDP login
- Added functionality to send files download URL to monitors

Media Player
- Worked on more MP configuration

Extra
- Minor update in report
```

**Sprint results**
```
Everything seems to have been met.
```

---

## 31/04/2024 - 07/05/2024
For the upcoming 3 weeks (including this one) it was the group's responsability to create and deliver sprints.

```
Frontend
- Fix scheduler page UI bugs
- Add some verifications to scheduler page
- Fix small bugs in Media page
- Research graphs for dashboard page
- Design CCT
- Work some more on the CCT mock up
- Improve some UI aspect

Backend
- Create last unit tests
- Add more integration tests
- Analyse schedule structure and fix it if needed

Media Player
- Complete the work on fetching media files for templates
- Try to finish configuration

Extra
- Review pending PRs and issues
- Create checkpoint 2 presentation

Monday (06/05/2024)
- Refactor code
- Work on technical debt
- Work on documentation
- Work on report
```

**Detailed version**
```
Frontend
- CCT
- Created page that allows us to view all existing templates
- The page already uses the information from the backend, missing the create template functionality
- The template editor page already allows for moving the divs around and resizing them

Other
- Fixed some problems with the animations
- Graphics framework has been chosen
- Added validations with explanations to the Scheduler ui
- General ui fixes

Backend
- Sending the files' download links to the MediaPlayer
- Updated schedule and templateGroup entities and their logic
- Unit tests for templateGroup, templateWidget , monitorGroup

Media Player
- Downloading the files from the backend is done
- Continued to work on the configuration

Deployment
- Initial attempts at deployment using nginx and a production docker-compose
- We were able to host the backend in the server that we were given and then through a public broker communicate in different networks (in different houses)
```

**Sprint results**
```
No documentation was found related to this.
```

---

## 08/05/2024 - 14/05/2024

```
Frontend
- Continue CCT Development
- Add option to remove files
- Add option to remove templates
- Add 'select group' verification in the schedule
- CRUD rules for schedule
- Start adding visual calendar

Backend
- Finish Integration tests
- Add logs for the monitors and finish adding remaining backend logs
- Change the way templateGroup is being sent
- Add some missing logic when adding a monitor and getting the respective templateGroups

Extras
- Refactoring code and removing unused endpoints

Media Player
- Start implementation of the schedule
- Send logs to backend
- Attempt to finish configuration
```

**Detailed version**
```
No documentation was found related to this.
```

**Sprint results**
```
No documentation was found related to this.
```
---

## 15/05/2024 - 21/05/2024
No sprint was done for this week, however, by the end of the week, as the ending date was getting closer, Pedro decided to get back to team managing and created the following, even if simple, sprint based on the detailed version provided by them.

```
Extras
- Plan and organize what needs to be removed from our "to implement" features;
- Decide current sprint priorities for features;
- Work on said features, bugs and alike;
- Deploy app and test it;
- Continue working on the report;
- Plan commercial video's sketch, transcript and date to film
```

**Detailed version**

The sprint report (done by the team without Pedro's supervision) simply addresses the following
```
Checkpoint 20/05/2024
- Maioria das funcionalidades planeadas funcionais
- Imagem de Linux do Media Player funcional
- Deployment do backend + mosquitto na porta 80
- MediaPlayer consegue se reconectar depois de restarts/falha de internet
```

**Sprint results**
```
Not finished
- Minor frontend visual bugs
- Send rules to monitor when be reconnects
- Login/roles
- Visual aspect (widgets)
```

---

## 22/05/2024 - 28/05/2024
This was the last sprint ever created for the subject TQS took too much time from us and we aimed to have everything done this week in terms of PI (i.e. the product should be released and/or should be ready for deployment within DETI's televisions).

To guarantee that we would meet the deadlines for delivery, Pedro decided to divide the group into sub-groups to tackle each task more efficiently.

- Video editing was done by Tomas & Pedro (production involved everyone);
- Demo was done by Joao and Tomas;
- Poster was done by Rafael, Diogo & Miguel.

```
Frontend
- Check if delete is working correctly;
- Create issues on github;
- Document frontend and add some comments when needed;
- Work on Technical Debt.

Backend
- Fix update error;
- Change some tests;
- Document backend and add some comments when needed;
- Work on Technical Debt.

Media Player
- Fix problems found in the last week;
- Make a proper linux image;
- Try to make widgets more consistent (sizes, fonts, etc);
- If there is time, work on extra features (static ip, screensaver, extra widgets);
- Work on Technical Debt;
- Document MP and add some comments when needed.

Extras
- Continue working on the report;
- Work on the documentation and PI tab on the docs website;
- Record scenes for commercial video;
- Edit video;
- Create DEMO video for our application;
- Create poster for PI;
- Contact STIC?;
- Ask students to test/play around with our application to get some feedback;
- Arrange things with Daniel?;
- Register our group for students DETI (submit PI's form)

Deadlines (not final, just to deliver to tutors)
Video - 26/05/2024 **by 5pm**
Poster - 26/05/2024 **by 5pm**
Demo - 27/05/2024 **by 10am**
```


**Detailed version**
```
Frontend
- N/A.

Backend
- Changed some tests;
- Small fixes.

Media Player
- Fix most of the problems from last week;
- Created a proper linux image;
- Made widgets more consistent across resolutions;
- Created screensaver;
- Created events widget;
- Finished documentation for mp setup and config.

Extra
- Added more information to the report across all fields;
- Checked if things worked correctly, but we're waiting for our final merge;
- Added information to the documentation and removed unnecessary parts;
- Made documentation navigation prettier and easier to interact with;
- Recorded all scenes for the video, edited it and is now waiting for the final approval;
- Created DEMO, edited it and is now waiting for the final approval;
- Created poster and is now waiting for the final approval;
```

**Sprint results**
```
Missed
- Work on Technical Debt;
- Create most issues on github;
- Document frontend and add some comments where needed;
- Document backend and add some comments where needed;
- Fix one Media Player problem from last week;
- Create static IP (this was an extra, so it won't be worked upon);
- Work on PI tab documentation;
- Merge all branches into dev.
```

------------------

This is the end of sprint creation and report.

Overall I, Pedro, feel like the team did a good job most of the times at meeting deadlines. Organization-wise the team lacked a bit and I wasn't capable of providing what was needed due to lack of experience in team leading. Even then, I feel like I learned a lot and the team has as well.