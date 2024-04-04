# Coworking Space Service Extension
The Coworking Space Service is a set of APIs that enables users to request one-time tokens and administrators to authorize access to a coworking space. This service follows a microservice pattern and the APIs are split into distinct services that can be deployed and managed independently of one another.

## Getting Started

### Project Structure
1. `app` folder - Consists application files
2. `db` folder - Consists the SQLs for creating databases and tables
3. Dockerfile - Used for building the docker image for the application
4. buildspec.yml - Used for CodeBuild project (Add the environment varibles used in this file to the CodeBuild project ) 

### Workflow
`Source Code (Github) --> CodeBuild --> ECR`


### Steps to release new builds
1. Clone the project repository and make the modifications for next release (for example changing the application code a bit).
2. Commit the changes to the Github account.  
3. CodeBuild will detect the change in the source code and automatically build and push the image to ECR. 