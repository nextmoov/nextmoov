[WIP]

# How to create a New Repository

As we tend to use micro-services architectures, you should create a repository for every component of your app : API, ETL, frontend, mobile app,...

Here is a step-by-step guide to do so

1. [Create Repository](https://github.com/new)
2. Name it _CLIENT_-_PROJECT_-_COMPONENT_
  
  > Example : _modalizy-services-api_

### Configure Repository

#### Base Branch : Develop
#### Locking Configuration

Use this locking configuration for non-feature branches : 

```
*[!feature/*]*
```

<img alt="Screenshot 2019-04-18 at 15 01 07" src="https://user-images.githubusercontent.com/4315469/56362750-e4c70300-61ea-11e9-9283-673075754395.png">
<img width="480" alt="Screenshot 2019-04-18 at 14 59 17" src="https://user-images.githubusercontent.com/4315469/56362716-d5e05080-61ea-11e9-85a2-b2b915562301.png">

### Slack Integration

Go to the client reporting channel #r-_CLIENT_
Type :
  ```github subscribe nextmoov/_CLIENT_-_PROJECT_-_COMPONENT_
