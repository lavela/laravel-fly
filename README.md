# Laravel + PostgreSQL Deployment on Fly.io

This repository contains a custom Dockerfile configuration for deploying a Laravel application with PostgreSQL on Fly.io. The default Fly.io image had issues with php8.2-swoole, which led to SSL negotiation errors when connecting to the PostgreSQL database:

```bash
SQLSTATE[08006] [7] could not send SSL negotiation packet: Resource temporarily unavailable (Connection: pgsql, SQL: (select * from ...))
```

This repository provides a custom solution by creating a Docker image without php8.2-swoole to ensure proper deployment and functionality.

## Problem

The official Fly.io image for Laravel applications is currently causing issues with the PostgreSQL connection due to the use of php8.2-swoole. The error occurs during database connection, making the deployment process unreliable.

## Getting Started

Follow the steps below to configure and deploy the application using this custom Docker setup.

 - Make sure the Dockerfile contained in the repository is correct to resolve the deployment issue.
