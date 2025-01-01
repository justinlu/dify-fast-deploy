# Dify Slim-Compose Deployment

[Click here to learn more about Dify](https://github.com/langgenius/dify)

## About this repository

This repository is mainly used as personal use, providing additional storage separation and extremely simplified deployment files based on the original Dify Compose file to simplify the deployment operation of Dify.

## About compose version

### docker-origin / Original Configuration

Original dify compose file, no modification.

### docker-slim / Slim Configuration

Extreme simplification based on the original configuration, using the default Weaviate as the vector database for data storage, and significantly simplifying non-essential configuration items and components, only retaining the Weaviate and Qdrant vector database configuration.

Removed configurations in slim version:

```
# Infrastructure
certbot

# Vector databases
tidb
couchbase-server
pgvector
pgvecto-rs
chroma
oceanbase
oracle
etcd / minio / milvus-standalone
opensearch / opensearch-dashboards
myscale
elasticsearch / kibana

# ETL type
unstructured
```

## Install / Deployment

> Warning: Please be sure to change the `SECRET_KEY` in the `.env` configuration file to ensure the security of your data, and you should never use any key from the public repository!

1. Go to `docker-slim` folder
2. Rename `.env.example` to `.env`
3. Modify the `.env` content as needed
4. If you need to store Dify data in a different path, modify the contents of `volumes` in `docker-compose.yaml` as needed
5. If you changed the storage path in step 4, copy the volumes folder to the target path as needed
6. Just start compose
