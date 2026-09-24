# Angga Kersana Munggaran

**Senior full-stack engineer, backend-leaning.** Seven years building hiring software at ASTRNT, from the product spec through to production and the incident calls in between.

I write the specification, build the thing, and keep it running. Most of my depth sits in backend services and the unglamorous parts around them: asynchronous processing, data modelling, and making a platform survive its own peak season.

Portfolio and full track record: **[anggakersana-dev.vercel.app](https://anggakersana-dev.vercel.app)**
LinkedIn: **[in/angga-munggaran](https://www.linkedin.com/in/angga-munggaran/)** · Email: **anggakersana@gmail.com**

## What I work with

| Area | Tools |
|---|---|
| Backend | TypeScript, Node.js, NestJS, PHP, Laravel, Lumen, REST API design |
| Data | MySQL, PostgreSQL, Redis (cache and queues), Elasticsearch |
| Frontend | React, Next.js, TypeScript, Tailwind CSS |
| Cloud and delivery | AWS (S3, DynamoDB, Elastic Beanstalk), Azure (Blob, Pipelines, Media Services), Docker, Azure DevOps CI/CD |
| Testing | Cypress and Puppeteer, on a no-mock end-to-end policy |

## What I have shipped

Seven years on one product family: HR technology for enterprise clients, as B2B SaaS. The work I am proudest of is the candidate assessment platform, asynchronous video interviews that removed the scheduling constraint from hiring at volume.

- **Asynchronous interviews with automatic scoring and a transcript summary**, so screening capacity stops depending on interviewer hours.
- **A chunked upload and server-side reconstruction path**, so a dropped connection never costs a candidate their answer.
- **An admission gate on concurrent sessions**, because concurrency is what the infrastructure costs and what a client agreement actually pays for.
- **A media quality gate** using ffmpeg silence and freeze detection, with a retake flow a human approves, so a bad recording does not silently fail a good candidate.
- **A production performance crisis at 2,500 concurrent candidates**, traced to N+1 queries, missing indexes and row-lock contention, fixed with query rewrites, an index and lock audit, and moving heavy work behind queues.

The numbers behind that, because they are checkable: 11,697 commits across 35 repositories, 1,661 Jira tickets at 93 percent completion, and 88 active months out of 88.

## Public code

- **[ShopeeMonitor](https://github.com/anggakersanamunggaran/ShopeeMonitor)** - real-time seller analytics for Shopee: NestJS API and a React dashboard, syncing through the Shopee Open Platform API v2.
- **[laravel-solid-starter](https://github.com/anggakersanamunggaran/laravel-solid-starter)** - a Laravel 12 REST API starting point: slim controllers, a service layer, repository pattern with contracts, typed DTOs, action classes.
- **[Blog-Api](https://github.com/anggakersanamunggaran/Blog-Api)** - architecture study: clean code, onion architecture, dependency injection, Redis Streams.
- **[nest-js-starter-kit](https://github.com/anggakersanamunggaran/nest-js-starter-kit)** - the NestJS setup I reach for.
- **[backend-assessment-python](https://github.com/anggakersanamunggaran/backend-assessment-python)** - a Python backend exercise.

## Currently

Going deep on .NET and C#, deliberately. Seven years across several stacks has given me breadth, and I would rather know one ecosystem properly than keep skimming four. Open to senior full-stack and product engineering work in Bandung or remote.
