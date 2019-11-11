# Services 

This document lists all services, both in development and planned, that are part of the Xenia project

## Current

### kim
kim is the primary frontend service that provides the main interactions for all users using the Xenia platform. kim will primarily interact with rock the main backend service, but is intended to be decoupled and isolated from all other services.
 
### rock
rock is the central backend service that will handle data aggregation and logic handling from other services and provide a RESTful api to the kim, the primary front end services. Although whatever database strategy is used, currently SQL via Postgres is used, rock should exist in the same deployment, and should be considered to be tightly coupled to it.    

### stark
This repo, stark, is meant to be used as the primary knowledge store for the Xenia project. It should be considered the source of truth for all questions related to the design and direction of Xenia and should be updated and maintained accordingly. 


## Planned

### pitt
pitt is the codename for what will become the 'match making' service. Rather than have the roomate matching algorithm be excuted in rock the main back end, this functionality is given its own service to reduce complexity down the line. 

### alfred  
As Xenia matures and approaches production and successive product updates it will require devops support. This is where alfred comes in, as it's meant to host our first iteration of our deployment pipeline. The specifics of said pipeline will be determined in the future as our resource requirements and availability becomes more clear. 