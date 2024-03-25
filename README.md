# my_voting_app
A mini micro-services voting application created by pods from dockerhub and hosted on kubernetes



application pod address on dockerHub
-  docker pull damton1/voting-results:latest
-  docker pull damton1/voting-pod
-  docker pull damton1/voting-results

Application Architecture : 

A Python webapp for voting between two parties linked to a redis database
A Redis queue for in-memory store of data from the user interface voting app
A Worker pod for processing data and serving as alinkage between the pods
A Postgres database to pull data from the worker pod
A Node.js webapp which pulls data from the postgres pod and relay it to the result app user interface in real-time
