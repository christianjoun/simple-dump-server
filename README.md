This is a Sample Go HTTP server that will spit all information of the requests it receives

Port: 8080

Available endpoints:
- /healthz
- /readyz
- /test200
- /test400
- /test401
- /test404


### Helm command for installing service chart:
$ helm install helm/simple-dump-server --namespace default --set 'ingress.fqdn=example.com' --name simple-dump-server

### Helm command for installing and running the integration test chart:
$ helm upgrade --install simple-dump-server-test-0 --namespace default-poc --set 'ingress.fqdn=example.com' helm/simple-dump-server-test  

$ helm test simple-dump-server-test-0 --debug
