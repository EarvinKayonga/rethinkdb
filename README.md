# RethinkDB from code source in a Docker Container

## 2 ways to Enjoy:

### Pulling images from Docker Hub (Recommended)

Docker Hub Repo: [https://hub.docker.com/r/earvin/rethinkdb/](https://hub.docker.com/r/earvin/rethinkdb/)

```
docker pull earvin/rethinkdb:latest #(optional)
mkdir data
docker run                \
--name db                 \
-d                        \
-p 8080:8080              \
-p 28015:28015            \
-p 29015:29015            \
-v data:/data             \
earvin/rethinkdb:latest

```

### Git Clone, building and running

Consider going through  **30 minutes of compilation though**

```
git clone git@github.com:EarvinKayonga/rethinkdb.git rethinkdb
cd rethinkdb
mkdir /data
docker build -t earvin/rethinkdb .

docker run              \
--name db               \
-d                      \
-p 8080:8080            \
-p 28015:28015          \
-p 29015:29015          \
-v data:/data           \
earvin/rethinkdb

```

#### Requirements:

 * **Have Docker Installed**
