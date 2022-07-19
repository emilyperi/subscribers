### Subscribers RestAPI
This repository follows along an online tutorial for building a Rest API with the Express framework. The full tutorial was created by (Web Dev Simplified)[https://www.youtube.com/c/WebDevSimplified]

##### Middleware
The app uses middleware in `routes/subscribers.js` to route GET, POST, PUT and DELETE requests to appropriate functions that interact with a JSON database

##### Usage
Run `npm run devStart` in a terminal window. Then in another window run:

GET all subscribers
`curl http://localhost:3000/subscribers`

POST subscriber with `name` "Catra" and `subsribedToChannel` "Learn World Domination"
`curl --header "Content-Type: application/json" --request POST -d '{ "name": "Catra", "subscribedToChannel": "Learn World Domination" }' http://localhost:3000/subscribers`

GET single subscriber with `id=62d72c1362488487be203287`
`curl http://localhost:3000/subscribers/62d72c1362488487be203287`

PATCH subscriber wtih `id=62d72c1362488487be203287`
`curl --header "Content-Type: application/json" --request PATCH -d '{ "subscribedToChannel": "Adoras Vlog" }' http://localhost:3000/subscribers/62d72c1362488487be20328`
(alternatively change name with same format)

DELETE subscriber with `id=62d72c1362488487be203287`
`curl --request DELETE http://localhost:3000/subscribers/62d72c1362488487be203287`
