# New Project Checklist

So, you've been assigned a new project? Great ! \
Here are the simple steps to get you started. 

## Architecture

We work using a ["Micro-Services"](https://en.wikipedia.org/wiki/Microservices) approach. \
To follow it, your project should be divided in multiple separated components: 

- One or multiple API
- A web-client
- A mobile application
- ...

Start by taking a moment to think how you will divide your project. 
The point should be to maximize code-reuse across multiple projects.

## Create a repository for any component

- For a backend component (API,...), use our Backend Template : [nextmoov-template-backend](https://github.com/nextmoov/nextmoov-template-backend)
- For a frontend component, use our Frontend Template : [nextmoov-template-frontend](https://github.com/nextmoov/nextmoov-template-frontend)

That's it ! 
Our templates are filled with every conventions you should follow.
Our CI stack will ensure you follow these — and the CD stack will take care of launching your project on both staging and production environnements.

## Work on this repository

Read about our [Coding Flow](./CodingFlow) to learn how to work on this new repository of yours.
