# Simple microservice app

All the services on this app is run by the docker-compose file.

By using a single command it will spin up containers containing the services youn want to run.
In this case it spins the `main` and `sub` app.

These app are span up on different using ports and can be accessed by going to the designated urls
In this case - `localhost:80`, `localhost:80/api`

# Setup

1. Clone the project
2. run the following commands

```
docker-compose up #to spin up the containers
docker-compose down #to close and remove the containers
```
