# MongoDB Replica Set with Docker Compose

This is a sample project that demonstrates how to set up a MongoDB replica set using Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## Usage

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Create authentication key for replicaset
```
openssl rand -base64 756 > <path>
```
4. Set file owner as 999:999
```
chown 999:999 <key-path>
```
5. Change file permissions as 400
```
chmod 400 <key-path>
```
6. Change volume location in compose file to key path
7. Run docker compose up

## Configuration

The `docker-compose.yaml` file defines the configuration for the MongoDB replica set. By default, the replica set is configured with three nodes (`mongo`, `mongo1`, and `mongo2`) and a security keyfile at `./keyfile`. You can modify the configuration by editing the `docker-compose.yaml` file.