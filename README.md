# Dify Customized Deployment

[Click here to learn more about Dify](https://github.com/langgenius/dify)

## About this repository

This repository is primarily for personal use. Compared to the original Docker Compose, this repository has been significantly streamlined, with some performance parameter adjustments. For users in China, proxy settings and PIP mirror settings are pre-configured.

## What's Changed?

### Under /original

This is the original deployment solution for Dify, unmodified.

### Under /lite

This is the streamlined deployment solution for Dify. Compared to the original version:

- Split the Dify data storage path to the .env file for unified configuration.
- Add network proxy settings.
- Removed vector database support: QDrant, Milvus, MyScale, CouchBase, PGVector/PGVector-RS, TiDB, Chroma, Oracle, Relyt, OpenSearch, ElasticSearch, OceanBase, Opengauss.
- Removed middleware support.
- Adjust API Worker from 1 to 3.
- Adjust default ETL type to Unstructured.
- **\[Security\]** Team member invitation validity period reduced from 72 hours to 8 hours.
- **\[Security\]** Default Web service port changed from 80/443 to 8080/8443.
- Set the default PIP mirror source for Plugin Daemon to Aliyun.

## How to Deploy Dify

Refer to `/lite/README.md`.