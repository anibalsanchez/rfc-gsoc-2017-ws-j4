# GSOC 2017: Webservices in Joomla 4

*Welcome to the Joomla! Google Summer of Code (GSoC) 2017 project: Webservices in Joomla 4!*

* Project Description: Integrating a rest API endpoint (like API/) into the Joomla Core. More information is going to follow in the next days.
* Expected Results: Working REST API for the core. Including com_content as the reference implementation.
* Knowledge Prerequisite: PHP, RESTful Webservices. 
* Nice to have: Joomla MVC, Swagger, Knowledge of APIs.
* Difficulty: Medium to Hard
* Mentors: Matias Aguirre [@fastslack](https://github.com/fastslack, Anibal Sanchez [@anibalsanchez](https://github.com/anibalsanchez), George Wilson (https://github.com/wilsonge)

## RFC: Request for Comments

* Status: Draft

This document is intended to describe the current state of the general conversation about the scope of the *GSOC 2017: Webservices in Joomla 4* project.

Since there were several previous attempts to implement *Webservices in Joomla*, the focus of this particular project is to achieve a working project to provide a REST interface for Joomla 4. Joomla 4 will be released with this project as a tool for the community benefit.

## MVP: Minimum Viable Product

### Project Definitions

This is the main list of features for the MVP:

* REST API for Joomla Content (com_content)
  - /api for Articles
  - List Articles (/api/articles)
  - Retrieve a Article (/api/articles/999)
  - Create a Article
  - Update a Article
  - Delete a Article

* **Development**
  - *External project from J4*. PRO: Freedom to develop and propose core changes
  - Inclusion in the Core: Time constraints and harder to be accepted. Difficult to evolve.

* **Extensibility**: other extensions must be able to add new entry points. REST API for Joomla Contacts (com_contact)
  - /api for Contacts
  - List Contacts (/api/contacts)
  - Retrieve a Contact (/api/contacts/999)
  - Create a Contact
  - Update a Contact
  - Delete a Contact

* **API Key Authentication**: authentication based on a general token. Generate a api key per user (in com_users for us) and use this in header for auth.

* **Business Models**:
  - *Current JModels*: The state of the models is currently tightly coupled (populate state etc.) to web stuff. Not channel-agnostic. PRO: They are throughly tested. For example: High level hacks for simple read operations. [https://github.com/mbabker/jdayflorida-app/tree/master/libraries/api/controller](https://github.com/mbabker/jdayflorida-app/tree/master/libraries/api/controller)
  - Mini-Service Layer: Create a clean layer. E.g. Article management via JTable, featured and frontend tables.
 
 * **Unit Tests**: The project must include tests.
 
 * **Interfaces**:
  - JModelInterface
    - getItem
    - getItems
   
### Nice to have

* User Interface to configure
* Backwards compatibility with J3

### Out of the scope

* ACL at field level
* OAUTH
* Service Layer

## Comparable Products

* Joomla! Downloads - API [https://downloads.joomla.org/api-docs/](https://downloads.joomla.org/api-docs/)
* Joomla! Downloads - Private Repo [https://github.com/joomla/downloads.joomla.org](https://github.com/joomla/downloads.joomla.org)
* WP REST API v2 Documentation - [http://v2.wp-api.org/](http://v2.wp-api.org/). [REST API Handbook](https://developer.wordpress.org/rest-api/reference/posts/)
* Drupal 8 APIs - RESTful Web Services API - [https://www.drupal.org/docs/8/api/restful-web-services-api/restful-web-services-api-overview](https://www.drupal.org/docs/8/api/restful-web-services-api/restful-web-services-api-overview)
* Laravel RESTful Resource Controllers - [https://laravel.com/docs/5.1/controllers#restful-resource-controllers](https://laravel.com/docs/5.1/controllers#restful-resource-controllers)

## Other References

* **Aug 31, 2013 - GitHub - chrisdavenport/j3-rest-api: REST API for Joomla 3.x* - [https://github.com/chrisdavenport/j3-rest-api](https://github.com/chrisdavenport/j3-rest-api)
* **May 2, 2016** - GitHub - chrisdavenport/service: Experimental Service Layer for Joomla 3.x - [https://github.com/chrisdavenport/service](https://github.com/chrisdavenport/service)
* Three Years with the WordPress REST API - K. Adam White. [https://bocoup.com/blog/three-years-with-the-wordpress-rest-api](https://bocoup.com/blog/three-years-with-the-wordpress-rest-api) *... the answer was clear: there’s a lot of good features in WordPress, but the code foundation upon which they are built is uneven. The REST API endpoints provide a new foundation for future core feature development, a facade layer that abstracts the inconsistencies of the past...*

## Community Channels

* Joomla GSoC 2017: https://groups.google.com/forum/#!forum/jgsoc2017
* GSoC 2017 Idea's-Mentors List: https://docs.google.com/spreadsheets/d/1JnpspX_Uwh1Dk7iYqoQvtOVieSuRjP366PmzQPOYfHk/edit#gid=0
* Glip Channel: GSoC 17 Webservices 

## Definitions for the students

# What should be the place for a student to start with, (pointing them to the right place)
# Required Skills to join the project
# 1 Student Slot. Optional 1 more slot if it could be defended.

## Important Upcoming Dates

* Now - March 20: Proactive students will reach out to you and ask questions about your ideas list and receive feedback from your org so they can start crafting their project proposals.
* March 20 - April 3 16:00 UTC: Students will submit their draft proposals through the program website for you to give solid feedback on.
* April 3 - 16: Review all submitted student proposals with your org and consider how many you want to select and how many you can handle. Decide on the minimum/maximum number of student slots to request.
* April 17, 16:00 UTC: Deadline to submit slot requests (OAs enter requests)
* April 19, 16:00 UTC: Slot allocations are announced by Google
* April 19 - 24 16:00 UTC : Select the proposals to become student projects. At least 1 mentor must be assigned to each project before it can be selected. (OAs enter selections)
* April 24 - May 4: Google Program Admins will do another review of student eligibility
* May 4: Accepted GSoC students/projects are announced
* May 4 - 29: Community Bonding Period
* May 29: Deadline to notify Google Admins of an inactive student that you wish to be removed from the program
* May 30: Coding begins
* June 26-30: First evaluation period - mentors evaluate their students and students evaluate mentors
* July 24 - 28: Second evaluation period - mentors evaluate students, students evaluate mentors
* August 21- 29: Students wrap up their projects and submit final evaluation of their mentor
* August 29 - September 5: Mentors submit final evaluations of students
* September 6: Students passing GSoC 2017 are announced


