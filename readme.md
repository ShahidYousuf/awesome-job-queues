# Awesome Job Queues [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of background job and task queue libraries, job servers and brokers, the patterns around them, and reading on how they work.

## Contents

- [Libraries](#libraries)
	- [Python](#python)
	- [Ruby](#ruby)
	- [JavaScript and TypeScript](#javascript-and-typescript)
	- [Go](#go)
	- [Java and JVM](#java-and-jvm)
	- [.NET](#net)
	- [Elixir](#elixir)
	- [PHP](#php)
	- [Rust](#rust)
- [Framework integrations](#framework-integrations)
	- [Django](#django)
- [Job servers](#job-servers)
- [Workflow and durable execution](#workflow-and-durable-execution)
- [Database-backed queues](#database-backed-queues)
- [Brokers](#brokers)
- [Managed services](#managed-services)

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

### Ruby

- [Delayed::Job](https://github.com/collectiveidea/delayed_job) - Database-backed priority queue for background jobs, extracted from Shopify.
- [GoodJob](https://github.com/bensheldon/good_job) - Multithreaded, PostgreSQL-based Active Job backend for Rails that uses advisory locks and `LISTEN/NOTIFY`, with a web dashboard.
- [Que](https://github.com/que-rb/que) - Job queue for Ruby and PostgreSQL that locks jobs with advisory locks and can enqueue jobs in the same transaction as other data.
- [Resque](https://github.com/resque/resque) - Redis-backed library for creating background jobs, placing them on multiple queues and processing them later.
- [Shoryuken](https://github.com/ruby-shoryuken/shoryuken) - Thread-based Amazon SQS message processor with Active Job support.
- [Sidekiq](https://github.com/sidekiq/sidekiq) - Background job processor that runs many jobs concurrently in threads, backed by Redis, Valkey or Dragonfly.
- [Solid Queue](https://github.com/rails/solid_queue) - Database-backed Active Job backend for MySQL, PostgreSQL and SQLite that uses `FOR UPDATE SKIP LOCKED` where available.
- [Sucker Punch](https://github.com/brandonhilkert/sucker_punch) - Asynchronous job library that runs its queues inside the application process using concurrent-ruby.

### JavaScript and TypeScript

- [Agenda](https://github.com/agenda/agenda) - Job scheduling library for Node.js that stores jobs in MongoDB by default through a pluggable backend.
- [BullMQ](https://github.com/taskforcesh/bullmq) - Redis-based distributed queue for Node.js with an optional PostgreSQL backend and clients for Python, Elixir, .NET, Rust and PHP.
- [Graphile Worker](https://github.com/graphile/worker) - Job queue for PostgreSQL running on Node.js that can also take jobs created by PostgreSQL triggers and functions.
- [node-resque](https://github.com/actionhero/node-resque) - Redis-backed background jobs for Node.js with an API compatible with Resque.
- [pg-boss](https://github.com/timgit/pg-boss) - Job queue for Node.js that stores jobs in PostgreSQL and claims them with `SKIP LOCKED`, with cron scheduling.

### Go

- [Asynq](https://github.com/hibiken/asynq) - Redis-backed distributed task queue that processes tasks concurrently in worker goroutines.
- [River](https://github.com/riverqueue/river) - Transactional job queue backed by PostgreSQL or SQLite, with retries, scheduling, unique jobs and a web UI, plus compatible clients for Java, JavaScript, Ruby and Rust.

### Java and JVM

- [db-scheduler](https://github.com/kagkarlsson/db-scheduler) - Cluster-friendly task scheduler for Java that persists tasks in a single database table.
- [JobRunr](https://github.com/jobrunr/jobrunr) - Background job library for Java that runs fire-and-forget, delayed and recurring jobs from lambdas, stored in an SQL database or MongoDB, with a dashboard.
- [Quartz](https://github.com/quartz-scheduler/quartz) - Job scheduling library for Java that keeps jobs in memory or in a database through JDBC.

### .NET

- [Hangfire](https://github.com/HangfireIO/Hangfire) - Background job library for .NET that runs fire-and-forget, delayed and recurring jobs, with SQL Server storage and a built-in dashboard.
- [Quartz.NET](https://github.com/quartznet/quartznet) - Job scheduling library for .NET that keeps jobs in memory or in a database through ADO.NET.

### Elixir

- [Exq](https://github.com/akira/exq) - Redis-backed job processing library that uses a job format compatible with Resque and Sidekiq.
- [Oban](https://github.com/oban-bg/oban) - Job processing library backed by PostgreSQL, MySQL or SQLite.

### PHP

- [Action Scheduler](https://github.com/woocommerce/action-scheduler) - Job queue for WordPress plugins and themes that runs scheduled action hooks in the background without server access.
- [Laravel Queues](https://laravel.com/docs/queues) - Queue API built into Laravel with backends such as Amazon SQS, Redis and relational databases.
- [Symfony Messenger](https://symfony.com/doc/current/messenger.html) - Symfony component that dispatches messages to handlers through transports such as AMQP, Doctrine, Redis, Amazon SQS and Beanstalkd.

### Rust

- [apalis](https://github.com/apalis-dev/apalis) - Background task processing library with Redis, PostgreSQL, MySQL, SQLite and AMQP backends and cron scheduling, each as a separate crate.

## Framework integrations

### Django

- [Django Tasks framework](https://docs.djangoproject.com/en/stable/topics/tasks/) - Task API built into Django 6.0 that defines tasks and backends but provides no worker, so background execution needs a third-party backend.
- [django-celery-beat](https://github.com/celery/django-celery-beat) - Stores Celery periodic task schedules in the database and manages them from the Django admin.
- [django-celery-results](https://github.com/celery/django-celery-results) - Stores Celery task results with the Django ORM or cache framework.
- [django-rq](https://github.com/rq/django-rq) - Django integration for RQ that configures queues in Django settings.
- [django-tasks](https://github.com/RealOrangeOne/django-tasks) - Backport of Django's built-in Tasks framework.
- [django-tasks-db](https://github.com/RealOrangeOne/django-tasks-db) - Backend for Django's Tasks framework that stores tasks with the Django ORM and runs them with a `db_worker` command.

## Job servers

- [Faktory](https://github.com/contribsys/faktory) - Language-agnostic job server that holds jobs in queues for workers in any language to fetch through its API.
- [Gearman](https://github.com/gearman/gearmand) - Job server that farms out work to other machines or processes and can call functions across languages.

## Workflow and durable execution

- [Cadence](https://github.com/cadence-workflow/cadence) - Orchestration engine for long-running workflows, backed by Cassandra, MySQL or PostgreSQL.
- [Conductor](https://github.com/conductor-oss/conductor) - Durable execution platform for microservices and workflow graphs that originated at Netflix.
- [DBOS Transact](https://github.com/dbos-inc/dbos-transact-py) - Python library that adds durable workflows and queues to a program, built on PostgreSQL.
- [Hatchet](https://github.com/hatchet-dev/hatchet) - Orchestration engine for background tasks and durable workflows that uses PostgreSQL for durability, with Python, TypeScript, Go and Ruby SDKs.
- [Inngest](https://github.com/inngest/inngest) - Durable step functions that replace separate queues, state and scheduling, with SDKs in several languages. Source-available under SSPL.
- [Restate](https://github.com/restatedev/restate) - Platform for building resilient applications from durable building blocks such as workflows as code. Source-available under BSL.
- [Temporal](https://github.com/temporalio/temporal) - Durable execution platform whose server runs workflows written as code, handles intermittent failures and retries failed operations.
- [Trigger.dev](https://github.com/triggerdotdev/trigger.dev) - Platform for long-running TypeScript tasks and workflows with retries and queues.

## Database-backed queues

- [PGMQ](https://github.com/pgmq/pgmq) - PostgreSQL extension that provides SQS-style message queues with visibility timeouts, using only SQL objects and no background worker.
- [PgQ](https://github.com/pgq/pgq) - PostgreSQL extension that provides a generic queue with an API of SQL functions. Uses the pgqd daemon for ticks and maintenance.
- [PgQue](https://github.com/NikolayS/PgQue) - PgQ rebuilt in pure PL/pgSQL so it runs on managed PostgreSQL without a C extension or daemon. Uses an event log with per-consumer cursors.
- [pg_later](https://github.com/ChuckHend/pg_later) - PostgreSQL extension that runs SQL queries asynchronously and stores the results for later retrieval. Built on PGMQ.

## Brokers

- [NATS](https://github.com/nats-io/nats-server) - Messaging system whose JetStream persistence layer supports work-queue streams that delete each message once a consumer has read it.
- [RabbitMQ](https://github.com/rabbitmq/rabbitmq-server) - Multi-protocol messaging and streaming broker that supports AMQP 1.0, AMQP 0-9-1, MQTT and STOMP.
- [Redis](https://github.com/redis/redis) - In-memory data structure server with lists and streams that many job queue libraries use for storage.
- [Valkey](https://github.com/valkey-io/valkey) - Key-value data structure server forked from Redis before Redis moved to source-available licenses.

## Managed services

- [Amazon SQS](https://aws.amazon.com/sqs/) - Managed message queue service from AWS with standard and FIFO queues.
- [Azure Queue Storage](https://learn.microsoft.com/en-us/azure/storage/queues/storage-queues-introduction) - Azure service for storing large numbers of messages in queues inside a storage account.
- [Azure Service Bus](https://learn.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview) - Managed message broker on Azure with queues and publish-subscribe topics.
- [Cloudflare Queues](https://developers.cloudflare.com/queues/) - Message queues with guaranteed delivery, integrated with Cloudflare Workers.
- [Google Cloud Tasks](https://cloud.google.com/tasks/docs/dual-overview) - Managed service that dispatches and delivers large numbers of distributed tasks, including as HTTP requests to a target.
- [Supabase Queues](https://supabase.com/docs/guides/queues) - PostgreSQL-native message queues with guaranteed delivery on Supabase, built on PGMQ.
- [Upstash QStash](https://upstash.com/docs/qstash/overall/getstarted) - Serverless messaging and scheduling service that delivers messages to public HTTP endpoints.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.
