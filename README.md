# docker-lamp

## Getting Standard
#### 1.Install [Docker for Mac](https://www.docker.com/docker-mac) / [Docker for Windows](https://www.docker.com/docker-windows)

#### 2.Setup your workspace
Create your new workspace under the `docs/` directory.

#### 3.build & up
```
$ docker-compose up --build
```

#### 4.Access to your workspace
If you create 'example/' directory, You can access by `http://example.localhost`.  
Also if you need access to `example2/public/`, You can access by `http://example2.env` but then you have to edit and add hosts file as below.

```
127.0.0.1   localhost env
255.255.255.255 broadcasthost
::1             localhost env

127.0.0.1   example.env
```

### MySQL
```
user: root
password: password
```

### PhpMyAdmin
http://localhost:8080
```
user: root
host: mysql
password: password
```

### MailCatcher
http://localhost:1080
