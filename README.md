
# Echo server to test HTTP Post call

Http server to test HTTP POST call, we have two endpoints: successfulNotification and failureNotification.


## Message returned example:

![Print](https://github.com/samuelteixeiras/nodeEchoServer/blob/master/img/print.png)


## Running on local machine

clone the repository: git clone https://github.com/samuelteixeiras/nodeEchoServer.git

Go into the folder: `nodeEchoServer`

run the commands:

`npm install`

`npm start`

Open the browser and go to to http://localhost:3000

`/successfulNotification`

To send a successful notification to the server, use the following command:
### Successful Notification call example:
curl -X POST \
  http://localhost:3000/successfulNotification \
  -H 'content-type: application/json' \
  -H 'key: lpdlapdsa' \
  -d '{	"samuel":"test"}'

`/failureNotification`

To send a failure notification to the server, use the following command:

### Failure Notification call example:
curl -X POST \
  http://localhost:3000/failureNotification \
  -H 'content-type: application/json' \
  -H 'key: lpdlapdsa' \
  -d '{	"samuel":"test"}'

---

## Steps to create and run using a Docker container

docker build -t username/node-web-app .

docker run -p 8080:3000 -d username/node-web-app

Go to http://localhost:8080


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


---

Created based on https://github.com/socketio/chat-example.git
