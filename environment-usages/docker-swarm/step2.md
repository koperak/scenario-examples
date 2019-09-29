Utwórz sieć
`docker network create -d overlay swarmnet`{{execute T1}}

Uwórz usługę 'http' 

`docker service create --name http --network swarmnet --replicas 2 -p 80:80 katacoda/docker-http-server`{{execute T1}}


Sprawdź
`docker service ls`{{execute T1}}