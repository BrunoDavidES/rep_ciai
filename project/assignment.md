# Project Assignment
## Internet Applications Design and Implementation 2024/25

### Change log

- 2023-10-08: Initial version, this is a draft, still up for discussion and receiving feedback. Some points are marked "TBA" (e.g., "more to come"). All changes will be reported in this area.

## Introduction

The topic for this yeas is a social network built around painting, tactile
paintings, and its transformation pipelines. Users in our social network want to
post the results of their efforts while using
[Picastlo](https://picastlo.github.io), an [open-source
tool](https://github.com/picastlo/picastlo.github.io) to make tactile paintings. 

The functionalities involved include managing users and user authentication,
reading posts according to their visibility (groups/friends), make new posts
that text, and images, create, use, and share Picastlo pipelines. You will have
to analyse and modify the code in the prototype available that is designed as a
standalone client application. Namely, you will need to start by understanding
what is a pipeline and how to represent it on a database.

The actors in this systems are unauthenticated users and regular registered
Picastlo Users. Unauthenticated users can use Picastlo GUI and see posts,
download images and load pipelines in Picastlo GUI that are classified as
public.  

A user of the system can add a post in the social network, adding a picture and
a link to a pipeline stored in their profile. A processing pipeline is a
sequence of transformation as used in the shared prototype. A user can then see
a sequence of posts in a timeline that were posted publicly, directly by their
friends or by the members of groups that they belong to. Any user can then load
a pipeline, theirs or of another user, that (optionally includes the initial
image) into Picastlo, change the pipeline, and download the result to print in a
3D printer. In the end, The user may store the pipeline in their own profile,
customizing the visibility parameters (public, private, or friends only). A user
my sign in to the system. 

The operations that you must implement thoroughly need to support a client
application where it is possible to follow the workflow above. All other
operations and the data necessary can be mocked or introduced via seed data.
User registration can be mocked via seed data. 

**Data resources needed to make the application work do not need to be fully managed by the API and can be
introduced in the database using seed data creation procedures.**


## Technical Details

### Application Architecture

The application should be structured in microservices and each microservice
should implement a layered architecture and make available a REST API. The
microservices should be accessible through an API Gateway that implements the
full social network to present it to a client application. The application
should allow the uploading of images and pipelines and storing then in
databases.  

### Picastlo GUI

The code provided as open-source includes a GUI that processes images with
simple image transformations to produce tactile paintings. You should fork that
repository and use that code to implement your GUI for the social network.

### Requirements (in-progress)

#### Server-side system

The application should be implemented using the Spring framework and Kotlin. The
API should be documented using OpenAPI 3.0. The application should be developed
in a layered architecture with a  database in memory (H2). All the data
necessary to run the application should be preloaded into the database.

- Server applications should be SpringBoot, use Spring Data to connect to
  databases, and use H2 in memory database
- OpenAPI live documentation should identify resources and sub-resources clearly to support the full life-cycle of the resources.
- You should implement distributed model-based access control based on JWT tokens and capabilities.
- You need to store pictures in blobs in the database.
- more to come (TBA)

#### Client application

Your client-side single-page (web) application should implement a hierarchical
structure of components directly mapping a specification developed using IFML
and implementing the following user-stories. 

The application should be implemented using the React/Redux framework and
TypeScript. The client application should work together with the server-side
application to provide a full user experience. The connection to the server-side
application should be done using the OpenAPI specification. 

- more detailed requirements will be added.

### Evaluation Criteria (in-progress) 

#### Server-side system

- The correctness of the definition of raw resources being presented by the API
- The correctness and coverage of the database schema
- The architecture of the system, both the implementation and the reported architecture in the report (patterns).
- The modularization of the system, and the degree of data being persisted into proper domain-specific
  microservices is part of the evaluation
- The quality and amount of seed data used in the presented prototype
- Quality of documentation to deploy the application

#### Client application

- Quality of the React component structure
- Quality of the Redux state declaration
- Completeness of UI functionality
- Generic UI aesthetics


## Working Teams 

The project assignment should be done by teams of 3. If you cannot make a team of 3, talk to the instructor to authorize other solutions. 
Team registration will be necessary shortly (method TBA).

## Deliverables

All deliverables should be submitted by pushing them to the repository of the project in github classroom.

1. Microservice structure and global Architecture description 

2. Database schemas for each microservice

3. OpenAPI description per microservice and application (a pdf file printing the live specification of each server)

4. A Server-side application (a commit in the repository - tag SERVER)

5. Automatic unit and integration tests in a continuous integration style

6. Client-side application (a commit in the repository - tag CLIENT). 

7. IFML specification of the UI.

8. Presentation

9. Report

10. Video with the deployment procedure

11. Video with UI Demo (5 minutes showing all user stories)


### Submission details

The first submission will contain items 1 to 5, and 10. The second submission will contain items 6 to 11 (except 10). The second submission can update any element of the first submission.

You should receive the link to the assignment by email and instructions to register your team. Form your team and use that as your work repository, the **submissions with the prescribed tags** will be considered as the final ones for each part of the assignment. You can refine the server-side application in the second submission. 

## Important Dates

First submission: 2024-10-31

Second submission: 2024-12-19