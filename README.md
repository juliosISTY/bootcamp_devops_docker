# Docker Mini-project

## Build and test

To build and run the Dockerfile for test API run in your shell these commands:
```shell
docker build -t student-list_api:v1 .
docker run -d -p 5010:5000 -v ${PWD}/student_age.json:/data/student_age.json --name pozos-api student-list_api:v1
curl -u toto:python -X GET http://127.0.0.1:5010>/pozos/api/v1.0/get_student_age
```
We will in console line result like:
```json
{
  "student_ages": {
    "alice": "12", 
    "bob": "13"
  }
}
```
## Infrastructure As Code

To deploy your infrastructure run your docker-compose.yml with command:
```shell
docker-compose up -d
```
And test the url app in your browser.

## Docker Registry 

Go to the link of my Gitup [docker-registry](https://github.com/juliosISTY/-boocamp_devops_docker_tp5-docker-compose) to see how you can do to make it.
