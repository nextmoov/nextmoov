



# New Project Checklist

## Architecture
Your project should be divided in multiple separated components: 

- one or multiple API
- a web-client
- A mobile application

Start by taking a moment to think how you will divide your project. 
The point should be to maximum code-reuse across multiple projects for a client.

## Setup Walkthrough (TODO)


### Slack
1. If this is the first project for this client, create a channel named “r-<CLIENT>” 
“CLIENT” must be rigorously the same as the one used in AirTable
2. Create a channel name “p-<PROJECT>”
“PROJECT” must be rigorously the same as the one used in AirTable

### BitBucket
Create project in BitBucket
https://bitbucket.org/account/projects/create?owner=nextmoov
Create a repository for every component of your project :
https://bitbucket.org/repo/create?owner=nextmoov
BitBucket + Slack Integration
Add a new configuration to the BitBucket integration in Slack
It should post to r-<CLIENT> channel created earlier.
Copy the value of the webhook URL.
 https://nextmoov.slack.com/apps/new/A0F7VRDPE-bitbucket

For every repository you created for your project, add this webhook. 
On BitBucket, go to Repository > Settings > Webhooks > Add
	Name : Slack
	URL : The one you copied in step 1



