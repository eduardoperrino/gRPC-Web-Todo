
# gRPC-web

Simple example that shows gRPC working, just that :dash:

:warning: gRPC stubs needed have been generated before, so we just have to start **envoy**, **server** and **client**. 

# Launching Steps

## Start envoy
```
docker run -d -v "$(pwd)"/envoy.yaml:/etc/envoy/envoy.yaml:ro \
    -p 8080:8080 -p 9901:9901 envoyproxy/envoy:v1.16.1
```
## Install needed modules
```
npm install
```
## Launch server
```
node server.js
```
## Launch client (http://localhost:8081/)
```
npx webpack-dev-server client.js
```
