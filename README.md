# oraclexe-local-playground

This guide will walk you through setting up a OracleXE Playground and to connect to it with SQLPLUS

### Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed

### Getting started

1. Clone the repo:

```bash
https://github.com/homelab-2025/oraclexe-local-playground.git
```

2. Once done, you need to create a custom `.env` file based on the `.env.example` file
3. Then, you can create the database container using the command:

```bash
docker-compose up -d
```

Then you need to wait few minutes for the database to be ready

4. You check the database status by typing:

```bash
docker logs -f oracle
```

5. Finally, you can connect to the container using SQLPLUS by typing the following command (replace user, password and dbname if you change it (default database is XEPDB1)):

```bash
docker exec -it oracle sqlplus appuser/AppPass123@localhost/XEPDB1
```
