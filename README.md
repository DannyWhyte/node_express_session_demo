# sample project on how touse express sessions in node

steps
1) after cloning open terminal and type 'npm i'
2) call login api , on successful login the api will return user data with a session
3) pass the generated session in other api's headers with keyname 'sessionId'

for example import the following cUrl's:

1) Login 
`````````
    curl -X POST \
  http://localhost:8004/api/loginUser \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: ff2b85bf-f15e-9f36-6fea-5736046f43f3' \
  -d '{"data":{"loginId":"admin","password":"pass@123"}}'
`````````



2) test api
````````````
    curl -X POST \
  http://localhost:8004/api/test \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: b1760491-d36a-b5de-52be-fe16478152a7' \
  -H 'sessionid: AO0DxUasXQnN3cfFzKc0D8wVx9myKNZO' \
  -d '{"test":"pass"}'
````````