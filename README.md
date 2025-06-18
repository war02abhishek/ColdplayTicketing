**Frontend GOALs**

Login

Admin-  > create Concert
        > update seats of concert
        > get concert details
        
User    >get all concerts
        >get concert details
        >book ticket of particular concert
        >get ticket status


**Backend GOALs**

service-discovery
api-gateway(need properly working api gateway required while connecting frontend with backend)
notification-service(Mailing service is required for sending mail regarding latest queue number or we can simply mail that there is chnage kindly check,user can check via UI)
ticket-processing-service(consuming ticket request queue,updating cache and DB also counting queue number if there is no seat left)
ticket-service(pushing ticket requests in kakfka queue)

We will be using 
REDIS ->caching and finding queue number(need to see)
KAFKA ->queue for traffic handling
MONGODB->as DB
DOCKER

Deployments ->either kubernates or AWS if we can (will be challenging)
