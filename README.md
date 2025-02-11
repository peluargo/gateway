# Gateway

![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)

## About the project
The `Gateway` is a application focused only in redirecting the HTTP requests made by the account towards the corresponding microsservice registered in a **Discovery Server**.

![peluargo-app-discovery](https://github.com/account-attachments/assets/ff14b7b1-4e8e-47b6-804a-cdae42c61076)

### Discovery Server
The gateway is being used together with another project called [Discovery](https://github.com/peluargo/discovery-server), where all other microservice projects (just like this gateway) are being registered as an **Eureka Client** inside an **Eureka Service**.

#### The exposed port
The responsible for determining which port will be exposed to give access into the server is the gateway itself. So, the exposed port will be the port in which the gateway project is running.

#### Load balancing the request
The gateway also works as a load balancer when multiple instances of the same microservice are up, so he automatically balance the demand between the instances.

![peluargo-app-load-balancer drawio](https://github.com/account-attachments/assets/5db33353-61f1-4f3e-a254-ece6bf607792)
