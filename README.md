## Mongo DB Replica Set

This is a replica set with 3 nodes.

### How to run

```bash
docker compose up -d
```

### How to check

```bash
docker compose exec mongo1 mongosh --port 27017 --quiet
```

and then run the following command:

```javascript
show dbs
```

### How to stop

```bash
docker compose down
```

### How to connect

```bash
mongodb://127.0.0.1:27017,127.0.0.1:27018,127.0.0.1:27019/?replicaSet=rs0
```

### Limitations

If you have trouble connecting to the MongoDB replica set, make sure Docker is up and running. Make also sure that the `host.docker.internal` hostname can be resolved to the host machine’s IP address.

If `host.docker.internal` cannot be resolved on Linux, you must add a line in your `/etc/hosts` file to map `host.docker.internal` to the IP address `127.0.0.1`.
