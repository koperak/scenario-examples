Deploy nowej wersji aplikacji
`docker service update --update-parallelism 1 --update-delay 5s --image lherrera/webapp:2.0 webapp`{{execute T1}}

Zobacz co się dzieje
`while true; do curl host02; sleep 2; done`{{execute T2}}