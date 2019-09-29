Utwórz sieć
`docker network create --driver overlay webnet`{{execute T1}}

Uwórz usługę 'webapp' 

`docker service create --name webapp --replicas=3 --network webnet --publish 80:8000 lherrera/webapp:1.0`{{execute T1}}

Utwórz usługę 'redisdb' 
`docker service create --name redisdb --network webnet --replicas 1 redis:alpine`{{execute T1}}

Sprawdź usługi
`docker service ls`{{execute T1}}

Sprawdź usługę 'webapp'
`docker service ps webapp`{{execute T1}}

