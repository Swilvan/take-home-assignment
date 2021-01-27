# Project plan

### Architecture (TODO: more succinct!)
My vision for the architecture for this project will be almost exactly the same as the vision for one of the projects
I worked on in the past. I will setup a microservice architecture with an API gateway that serves the front-end and that 
communicates to at least one back-end service. I believe one of the most important success factors in a software project
is to make it easy to work on for multiple people. That means that these at least three services will run locally in their 
own docker containers that will be spun up by a single command (e.g. `make run.all` or something similar). I will structure
my work in a way where "least confident" and "most important" determine what I do first such that I have time for things that
are hard for me, or important for the assignment.

### Division of work in the team

Some of this is dependent on how the team is composed. How experienced is everyone? Are all of them specialists? How often
are we physically working together? I would want to decide upon an architecture/approach together with the team. Based on 
the approach the team has decided upon I would want to figure out the first 2 or 3 questions that need to be answered to 
enable the team to work on the stories (e.g. how do we structure the front-end and what language/library/framework will we use?
Similar for backend, persistence). If we have someone who is super experienced in any of the technical areas that we cover
I would want to ask them to propose concrete project setup. If we have someone who just came out of school I would want 
them either pairing with a more experienced person or at least checking in every couple of hours so we keep moving forward
and they learn as much as possible. Having setup the technical stuff I would want the team to start talking about API's 
so we can set up a future proof system. I want to break my API as little as possible but still give myself the highest
amount of freedom to change the code behind my (public facing?) API. Having finished the technical setup and the API's 
involved I would want the team to decide upon the specifics of how to implement the stories and divide work as we see fit.

### How will this break in production?

TODO: determine when code is complete 

### Tasks

- Setup Front-end using next
- Setup back-end grpc API
- Connect front-end to API service using grpc
- Setup 'internal' back-end service that the 'api' service calls to do work
- Connect grpc API service to 'internal' service
- Implement front-end part of stories 
- Implement back-end part of stories
- 'Future proof' system
    - add metrics/logging where lacking
    - add persistence layer