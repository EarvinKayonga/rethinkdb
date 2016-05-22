# RethinkDb from SOURCES in a Docker Container


To build and run:

```
docker build -t earvin/rethinkdb .
mkdir data
docker run -t db -d -p 8080:8080 -v data:/data rethinkdb-src
```

Requirements:

Have Docker Installed
