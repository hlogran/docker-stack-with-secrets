# docker-stack-with-secrets
A small practice of docker swarm stacks with external secrets

This is a Stacks example in which external secrets are used to set the postgres initial passowrd. To test it follow the following steps:

## Instructions to run
- Init swarm mode via the command `docker swarm init`
- Create the secret via the following command: `echo <"your_password"> | docker secret create psql_password -`
- Deploy the stack with: `docker stack deploy --compose-file docker-compose.yml <your_stack_name>`
