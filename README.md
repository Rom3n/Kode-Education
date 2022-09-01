Simple Golang API for creating notes

Redis in docker container
```console
foo@bar:~$ docker-compose up
```
To run:

```console
foo@bar:~$ go run .
```

Application will be listening on localhost:8080

API routes(POST only) are listed in main.go

localhost:8080/login,  to Login
localhost:8080/logout, to Logout)
localhost:8080/refresh, to Refresh token

```console
foo@bar:~$ curl -X POST localhost:8080/login --data '{ "username" : "username", "password" : "password" } '
```

localhost:8080/note, to Create Note

```console
foo@bar:~$ curl -X POST localhost:8080/note --data '{"user_id": 1, "title": "test" } '
```