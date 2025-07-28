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

>service-discovery

>api-gateway(need properly working api gateway required while connecting frontend with backend)

>notification-service(Mailing service is required for sending mail regarding latest queue number or we can simply mail that there is chnage kindly check,user can check via UI)

>ticket-processing-service(consuming ticket request queue,updating cache and DB also counting queue number if there is no seat left)

>ticket-service(pushing ticket requests in kakfka queue)

We will be using 
>REDIS ->caching and finding queue number(need to see)

>KAFKA ->queue for traffic handling

>MONGODB->as DB

>DOCKER

Deployments ->either kubernates or AWS if we can (will be challenging)



**ScreenShots**
<img width="1345" height="269" alt="image" src="https://github.com/user-attachments/assets/0621c84d-4adb-4d9c-bdd9-8a59cff9a280" />
<img width="1364" height="369" alt="image" src="https://github.com/user-attachments/assets/b8c30367-875d-4bba-888f-24e081e0efc4" />

<img width="1120" height="543" alt="image" src="https://github.com/user-attachments/assets/8a5e7ebe-de31-46a6-9293-8ce476b7d020" />


Creates a private network (like coldplay-latest_default)
Assigns each container an internal IP (e.g., 172.18.0.x)
Services talk to each other using these internal IPs or service names
<img width="1336" height="313" alt="image" src="https://github.com/user-attachments/assets/17f6c2fc-47c2-4dc9-a3cc-233ae1afd66b" />




Now localhost:8080 Works for You
we are exposing ports like this in docker-compose.yml:
ports:
  - "8080:8080"
This means:
Docker maps container port 8080 → host machine port 8080
You can access your API Gateway at http://localhost:8080 from your browser
<img width="661" height="127" alt="image" src="https://github.com/user-attachments/assets/15aba8ef-829a-4566-b4e3-9964ffbec2cf" />
<img width="452" height="96" alt="image" src="https://github.com/user-attachments/assets/9bfe9702-06f2-42d0-ae67-8366ec5ad1ed" />







