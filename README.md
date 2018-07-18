
# Echo server for post notifications test

/successfulNotification

/failureNotification


## Steps

docker build -t <your username>/node-web-app .

### just to check  
docker images
docker run -p 8080:3000 -d <your username>/node-web-app


## Successful Notification call example:
curl -X POST \
  http://localhost:8080/successfulNotification \
  -H 'content-type: application/json' \
  -H 'key: lpdlapdsa' \
  -d '{
	"samuel":"test"
}'


## Failure Notification call example:
curl -X POST \
  http://localhost:8080/failureNotification \
  -H 'content-type: application/json' \
  -H 'key: lpdlapdsa' \
  -d '{
	"samuel":"test"
}'
