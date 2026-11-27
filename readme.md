# Awesome Job Queues [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of background job and task queue libraries, job servers and brokers, the patterns around them, and reading on how they work.

## Contents

- [Libraries](#libraries)
	- [Python](#python)
- [Framework integrations](#framework-integrations)
	- [Django](#django)
- [Database-backed queues](#database-backed-queues)

## Libraries

### Python

- [Celery](https://github.com/celery/celery) - Distributed task queue that supports RabbitMQ, Redis, Amazon SQS and Google Pub/Sub as message transports.
- [Django Q2](https://github.com/django-q2/django-q2) - Multiprocessing distributed task queue for Django, a maintained fork of Django Q.
- [Dramatiq](https://github.com/Bogdanp/dramatiq) - Distributed task processing library with RabbitMQ and Redis brokers.
- [Huey](https://github.com/coleifer/huey) - Task queue that can store tasks in Redis, PostgreSQL, SQLite, the file system or memory.
- [PgQueuer](https://github.com/janbjorge/pgqueuer) - PostgreSQL-backed job queue whose workers claim jobs with `FOR UPDATE SKIP LOCKED` and wake on `LISTEN/NOTIFY`.
- [Procrastinate](https://github.com/procrastinate-org/procrastinate) - PostgreSQL-based task queue with periodic tasks, retries, task locks and Django integration, usable from sync and async code.
- [RQ](https://github.com/rq/rq) - Job queue backed by Redis or Valkey that runs jobs in the background with workers.
- [SAQ](https://github.com/tobymao/saq) - Job queue built on asyncio with Redis or PostgreSQL backends and an optional monitoring UI.
- [Taskiq](https://github.com/taskiq-python/taskiq) - Asynchronous distributed task queue that runs both sync and async functions and integrates with FastAPI and AIOHTTP.

## Framework integrations

### Django

- [Django Tasks framework](https://docs.djangoproject.com/en/stable/topics/tasks/) - Task API built into Django 6.0 that defines tasks and backends but provides no worker, so background execution needs a third-party backend.
- [django-celery-beat](https://github.com/celery/django-celery-beat) - Stores Celery periodic task schedules in the database and manages them from the Django admin.
- [django-celery-results](https://github.com/celery/django-celery-results) - Stores Celery task results with the Django ORM or cache framework.
- [django-rq](https://github.com/rq/django-rq) - Django integration for RQ that configures queues in Django settings.
- [django-tasks](https://github.com/RealOrangeOne/django-tasks) - Backport of Django's built-in Tasks framework.
- [django-tasks-db](https://github.com/RealOrangeOne/django-tasks-db) - Backend for Django's Tasks framework that stores tasks with the Django ORM and runs them with a `db_worker` command.

## Database-backed queues

- [PGMQ](https://github.com/pgmq/pgmq) - PostgreSQL extension that provides SQS-style message queues with visibility timeouts, using only SQL objects and no background worker.
- [PgQ](https://github.com/pgq/pgq) - PostgreSQL extension that provides a generic queue with an API of SQL functions. Uses the pgqd daemon for ticks and maintenance.
- [PgQue](https://github.com/NikolayS/PgQue) - PgQ rebuilt in pure PL/pgSQL so it runs on managed PostgreSQL without a C extension or daemon. Uses an event log with per-consumer cursors.
- [pg_later](https://github.com/ChuckHend/pg_later) - PostgreSQL extension that runs SQL queries asynchronously and stores the results for later retrieval. Built on PGMQ.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.
