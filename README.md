# mysql-cluster-docker-compose
Applied DevOps Assignment-3 				25/03/2021

## Requirements:
- ` sudo apt-get install docker.io ` 
- ` sudo apt-get install docker-compose ` 

## How to Start:

### start all the services using following cmd:

- ` docker-compose up -d `

### To verify everything went well by executing management container :

- ` docker exec -it management1 ndb_mgm `

### Run show command to see the configuration output :

```
-- NDB Cluster -- Management Client --
ndb_mgm> show
Connected to Management Server at: 198.168.0.2:1186
Cluster Configuration
---------------------
[ndbd(NDB)]	2 node(s)
id=11	@198.168.0.4  (mysql-8.0.23 ndb-8.0.23, Nodegroup: 0, *)
id=12	@198.168.0.5  (mysql-8.0.23 ndb-8.0.23, Nodegroup: 0)

[ndb_mgmd(MGM)]	2 node(s)
id=1	@198.168.0.2  (mysql-8.0.23 ndb-8.0.23)
id=2	@198.168.0.3  (mysql-8.0.23 ndb-8.0.23)

[mysqld(API)]	2 node(s)
id=21	@198.168.0.9  (mysql-8.0.23 ndb-8.0.23)
id=22	@198.168.0.10  (mysql-8.0.23 ndb-8.0.23)

ndb_mgm> exit


```

### Run the following command and login to the MySQL node :

- ` docker exec -it mysql2 mysql -uroot -p ` 

- `Enter password: <pucsd> `


### stop all the services and remove the container using following cmd:

- ` docker-compose down `
