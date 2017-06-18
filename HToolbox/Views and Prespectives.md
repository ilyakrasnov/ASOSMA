[allReady documents](https://github.com/PhillipKatz/allReady/tree/master/docs)


About the documentation:
Currently, most of the introductions and documentations are left blank, with placeholders at every aspect except the installation guide, the git guide, and an unfinished event-starting guide.


Database: Web API written in ASP.NET connects with JSON

Stakeholders
=============
* **Assessors**, who check for compliance.
Working in tandem with the allReady staff, relying on their results and handing requests and feedback.
  * Red Cross: (Director: @Jim McGowan)

* **Communicators**, who create documents and training.
Most of the documents are yet to be written, with the exception of the "getting started" tutorials for volunteers, which were written by allReady's core-developers
  * Github contributors

* **Developers**, who create the system / Maintainers, who evolve and fix the system
  * ***Core developers***: Staff skilled in management, knowledgeable in programming; mainly in Web, SQL, .NET, and AngularJS
    *	Web team (Rohit, Elizabeth, Matt, Dan, Daniel, Glen, Connie)
    *	Mobile team: (Jimmy, Dmitry, Parashuram, Louis, Guillaume)
  * ***Volunteering coders***:
    * open-source contributors who volunteer to work on the improvement of allReady

* **Production Engineers**, who are responsible for the deployment environment.
 * Core developers: Staff skilled in management, supervising and directing the development of allReady; 
	Seth Juarez (technical)
	Dmitry Lyalin (Senior Product Manager)
	Brady Gaster (Program Manager)
	Kirupa Chinnathambi (Senior Program Manager)
	Pranav Rastogi (Program Manager)
	Tarvis Lowdermilk (UX designer)
	Zlatko Knezevic (Program Manager)
	Jeff Fritz (Senior Program Manager)
	

* **Suppliers**, who provide parts of the system.
External companies which provide tools/ professional advisory/ software infrastructure
Microsoft (contributing working platform, free server use and storage, and professional advisory and guidance) and various contributors

* **Support Staff**, who help people to use the system.
Technical staff, who help participants with hardware installation
Volunteers with various helpful skills during the emergency of unexpected disasters
Various others. For example, people who help raise readiness in a town by assisting in the installation of smoke detectors wherever the residents can't do so on their own

* **System Administrators**, who keep it running.
Main manager (Richard Campbell)
Advisors from Microsoft (backlog /pool / task-sharing management , operation monitoring and various logistics)

* **Testers**, who verify that it works.
Every programmer (core developer or contributor) is required to make his own test and make sure his addition / revision works well.

* **Users**, who have to use the system directly.
The organizations which physically deal with the disaster by aiding the locals, and the aided victims of the disasterous event.
Examples for emergency services: Red Cross, Police, Fire-fighters...
Examples for victims: people from towns caught in hurricane/earthquake/forest fires 


**Context Diagram**
All of the involved parties around allReady
![context-diagram](https://github.com/turner11/ASOSMA/blob/master/HToolbox/imgs/Context%20Diagram.png)
The majority of allReady's views are involved with either git/github or Microsoft.


**allReady's Design**


***allReady's data-flow design***
Storage and flow of information
![data-flow](https://github.com/turner11/ASOSMA/blob/master/HToolbox/imgs/data_flow.jpg)
The database is shared between all supported platforms (mobile and web-browsers). The information is stored in Microsoft Philantropies' servers.

**Dependencies**
![dependencies](https://github.com/turner11/ASOSMA/blob/master/HToolbox/imgs/graph.png)
![slices](https://github.com/turner11/ASOSMA/blob/master/HToolbox/imgs/slices.png)
The code seems to be a bit tangled, though well-categorized.

**allReady's complexity score**
![complexity-score](https://github.com/turner11/ASOSMA/blob/master/HToolbox/imgs/complexity.png)
The XS Configuration is a set of thresholds for "Fat" and "Tangles" at different levels of composition.
Fat indicates "too much stuff" in one place and is measurable at every level of composition - Design, Namespace, Class and Method.
Cyclomatic Complexity is used as a measure of Fat at the method level - the number of dependencies in the child dependency graph is used at the other levels.
For the purposes of XS, tangles are only measured at the design level, i.e. cyclic dependencies between namespaces.
Both Fat and Tangles are measured as the percentage by which the threshold is exceeded. This percentage is multiplied by the size of the item so that the Average XS can be read as a percentage of the code-base.
allReady's app is sparse at its structure (reasonable for a project largely developed by volunteers), and is somewhat tangles.


Challenges for this project
============================
* In all disaster scenarios, the system has to be at least as reliable as "pen and paper". Some disasters may render crucial infrastructures inoperable, thus suitable solutions have to be prepared ahead of time;
  - for example, in case internet connecivity is weakened or lost at the disaster site, allReady's data transfer can be disrupted and resumed. If necessary, vehicles with wi-fi are brought to the site to allow a complete transfer.
* Known bugs / issues:
  - Missing lots of docmunetation
  - [Individual volunteers are unable to contact the admins unless they are part of a registered organization](https://github.com/HTBox/allReady/issues/1929)
  - [Inconsistant naming in code](https://github.com/HTBox/allReady/issues/1940)
  - [In-app map does not support Internet Explorer](https://github.com/HTBox/allReady/issues/1550)
  - [Missing part in tutorial about sql handling](https://github.com/HTBox/allReady/issues/1844)
  - [Volunteers are not messaged / contacted yet in an ordered fasion](https://github.com/HTBox/allReady/issues/1842)
  
  
