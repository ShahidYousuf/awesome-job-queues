# Awesome Job Queues [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of background job and task queue libraries, job servers and brokers, the patterns around them, and reading on how they work.

## Contents

- [Libraries](#libraries)
	- [Python](#python)
- [Database-backed queues](#database-backed-queues)

## Libraries

### Python

- [Celery](https://github.com/celery/celery) - Distributed task queue that supports RabbitMQ, Redis, Amazon SQS and Google Pub/Sub as message transports.
- [Dramatiq](https://github.com/Bogdanp/dramatiq) - Distributed task processing library with RabbitMQ and Redis brokers.
- [Huey](https://github.com/coleifer/huey) - Task queue that can store tasks in Redis, PostgreSQL, SQLite, the file system or memory.
- [RQ](https://github.com/rq/rq) - Job queue backed by Redis or Valkey that runs jobs in the background with workers.
- [Taskiq](https://github.com/taskiq-python/taskiq) - Asynchronous distributed task queue that runs both sync and async functions and integrates with FastAPI and AIOHTTP.

## Database-backed queues

- [PGMQ](https://github.com/pgmq/pgmq) - PostgreSQL extension that provides SQS-style message queues with visibility timeouts, using only SQL objects and no background worker.
- [PgQ](https://github.com/pgq/pgq) - PostgreSQL extension that provides a generic queue with an API of SQL functions. Uses the pgqd daemon for ticks and maintenance.
- [PgQue](https://github.com/NikolayS/PgQue) - PgQ rebuilt in pure PL/pgSQL so it runs on managed PostgreSQL without a C extension or daemon. Uses an event log with per-consumer cursors.
- [pg_later](https://github.com/ChuckHend/pg_later) - PostgreSQL extension that runs SQL queries asynchronously and stores the results for later retrieval. Built on PGMQ.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.
