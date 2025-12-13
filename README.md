# Homelab
This repo holds the IaC for my dockerised homelab. 
It's primarily used as a media server, but also does adblocking/DNS and some other things!

## OS
This repo, at the time of writing, is deployed on an n100 mini pc running debian. The setup was as simple as creating a user, installing docker and starting Doco-CD with Docker Compose, everything from then on was managed via IaC.

## GitOps with Doco-CD
This whole setup is deployed by the incredible [Doco-CD](https://github.com/kimdre/doco-cd). It acts as a Docker equivalent of the more common Kubernetes based GitOps tools, ArgoCD and Flux. You can see the .doco-cd.yml config file in the root of this repo that points Doco at the apps folder, deploying each of the docker compose files. 

## Sops
Secrets are encrypted using SOPS. For a guide on how to, see here: https://github.com/kimdre/doco-cd/wiki/Encryption

## Paths
I've configured all config paths to be stored in /srv/docker/<application_name>.

## Backups
Coming soon!
