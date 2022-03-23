
# Echo server to test HTTP Post notifications

/successfulNotification

/failureNotification


## Steps to create and run docker container

docker build -t username/node-web-app .

docker run -p 8080:3000 -d username/node-web-app



## After Deploy call the server:

### Successful Notification call example:
curl -X POST \
  http://localhost:8080/successfulNotification \
  -H 'content-type: application/json' \
  -H 'key: lpdlapdsa' \
  -d '{	"samuel":"test"}'


### Failure Notification call example:
curl -X POST \
  http://localhost:8080/failureNotification \
  -H 'content-type: application/json' \
  -H 'key: lpdlapdsa' \
  -d '{	"samuel":"test"}'

## Message returned:

![Print](https://github.com/samuelteixeiras/nodeEchoServer/blob/master/print-page.png)


Created based on https://github.com/socketio/chat-example.git
