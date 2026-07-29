# Docker Container Deployment

## Objective

Install Docker on Ubuntu Server and deploy a web service using containers.

## Environment 

- Ubuntu Server
- Kali Linux
- VirtualBox Host-only Network


Ubuntu IP:

```
192.168.56.101
```

## Installing Docker

Docker was installed:

```bash
sudo apt install docker.io -y
```

Docker version:

 
```bash
docker --version
```

Result:


```
Docker version 29.1.3
```

## Docker Service

 
Docker service status was checked:

 
```bash
sudo systemctl status docker
```
 
Result:

 
```
active (running)
```

## Testing Docker Installation

 
A test container was started:

 
```bash
sudo docker run hello-world
``` 

Result:

```
Hello from Docker!
```

This confirmed that Docker can successfully run containers.


## Running Nginx Container


Nginx image was downloaded:


```bash

sudo docker pull nginx

```
 
Container was created:


```bash

sudo docker run -d -p 8080:80 --name webserver nginx

```

Port mapping:
 
```

Ubuntu Server port 8080

        |

        ↓

Docker Container port 80

```


## Container Verification
 
Running containers:


```bash

sudo docker ps

```

Result:


```
nginx container running

```


## Network Testing


From Kali Linux:


```bash

nmap 192.168.56.101

```


Detected:


```
8080/tcp open
```


Web access test:


```

http://192.168.56.101:8080

```

 
Result:

 

```

Welcome to nginx!

```

## Docker Logs


Container logs:


```bash

sudo docker logs webserver

```

Logs confirmed that the Nginx container received requests.

 

---

## Conclusion

Docker was successfully installed and tested.

An Nginx web server was deployed inside a container and accessed from Kali Linux through the Host-only network.
