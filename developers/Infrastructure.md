# Infrastructure

## Table of Content

{{TOC}}

## Stack

- Rancher : 
- Drone : CI/CD Pipelines
- Sentry : Error Tracking
- Cabot

Domain Name
All domains are purchased and managed by OVH
See OVH account in 1Password
They all point to DigitalOcean NS servers
Infra-related domain name point to the IP of the Host hosting Traefik for that Stack
Components Config
Rancher
Stack

Name
<client>-<project>-<staging|production>

Hosts

Name
<client>-<project>-<staging|production>-node-<node-id>
Provider
DigitalOcean
Datacenter
AMS3
OS
Ubuntu ? CoreOS?
Tags
<staging|production>=true
<client>-<project>=true
<stack>-trafiek=true



Adding node-N to every host name will allow us to scale horizontally any service.
Don’t use project=<client-id>-<project-id> because a same tag (project) can’t be applied with multiple value on one host. That would block us to have multiple project on 1 host.

