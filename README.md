## Requirements
- Develop a ruby client application to fetch list of programming_languages from this server
  - Command line specification:
    - `$ ruby robot_api_client.rb [OUTPUT_FORMAT(csv or json)] [BASIC_AUTH_ID] [BASIC_AUT_PASSWORD]`
- Write tests for your ruby client application using `RSpec Mock`
- Optional
  - Implement error handlings

### Expected output example
- json
```
$ ruby robot_api_client.rb json someId somePassword
[
  {
    "code": "ruby",
    "displayName": "Ruby"
  },
  {
    "code": "python",
    "displayName": "Python"
  },
  {
    "code": "java",
    "displayName": "Java"
  }
  {
    "code":"html",
    "displayName": "html"
   }
]
```

- csv
```
$ ruby robot_api_client.rb csv someId somePassword
code,displayName
ruby,Ruby
python,Python
java,Java
```
## How to develop
- Clone this repository and build a local enviroment.
- Create another repository to develop a ruby client application which can interect with the server.

<br>
This application is also dockerized. 
if you use docker

```
$ docker-compose up 
```
then you can access to `http://localhost`

#### Basic auth
Id and password are written in docker/web/nginx.Dockerfile.

#### API
- GET /programing_languages


## How to submit
- Send your GitHub repository URL to a person in charge.
