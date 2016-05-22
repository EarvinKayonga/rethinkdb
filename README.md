# RethinkDB from code source in a Docker Container

## 2 ways to Enjoy:

### Pulling images from Docker Hub (Recommended)

```
docker pull earvin/rethinkdb:latest #(optional)
mkdir data
docker run -t db -d -p 8080:8080 -v data:/data earvin/rethinkdb:latest

```

### Git Clone, building and running

```
git clone rethinkdb
cd rethinkdb
mkdir /data
docker build -t earvin/rethinkdb .
docker run -t db -d -p 8080:8080 -v data:/data earvin/rethinkdb

```

#### Requirements:

 * **Have Docker Installed**
