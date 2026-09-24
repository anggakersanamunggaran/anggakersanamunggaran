<div align="center">

# Angga Kersana Munggaran

**Senior full-stack engineer · backend-leaning**

Seven years building hiring software at ASTRNT, from the product spec through to production and the incident calls in between.

[![Portfolio](https://img.shields.io/badge/anggakersana--dev.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://anggakersana-dev.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/angga-munggaran/)
[![Email](https://img.shields.io/badge/anggakersana@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:anggakersana@gmail.com)

</div>

---

I write the specification, build the thing, and keep it running. Most of my depth sits in backend services and the unglamorous parts around them: asynchronous processing, data modelling, and making a platform survive its own peak season.

## What I work with

**Backend**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![Lumen](https://img.shields.io/badge/Lumen-E74430?style=flat-square&logo=lumen&logoColor=white)

**Data**
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Cloud and delivery**
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Testing**
![Cypress](https://img.shields.io/badge/Cypress-69D3A7?style=flat-square&logo=cypress&logoColor=white)
![Puppeteer](https://img.shields.io/badge/Puppeteer-40B5A4?style=flat-square&logo=puppeteer&logoColor=white)

---

## What I have shipped

Seven years on one product family: HR technology for enterprise clients, sold as B2B SaaS. Every story below starts the same way, with someone describing a problem we had no infrastructure for yet. The underdog arc, except the training montage is a changelog.

**Act one. The scheduling problem.**
Hiring at volume used to cost interviewer hours, one calendar slot at a time. We built asynchronous video interviews with automatic scoring and a transcript summary, so a candidate answers on their own clock and screening capacity stops depending on how many interviewers happen to be free that week.

**Act two. The candidate who lost their answer.**
A dropped connection in the middle of a recording used to cost a candidate their entire attempt. So the answer upload became a chunked path with server-side reconstruction: the pieces land as they are sent, and the server rebuilds the file. The proctoring audio stream, the part with no package behind it, is the one I wrote myself. A bad connection now costs seconds, not an interview.

**Act three. The recording nobody could score.**
A silent or frozen recording used to reach a reviewer looking like a completed answer, which quietly fails a good candidate for the crime of owning a bad microphone. We put a quality gate in front of it using ffmpeg silence and freeze detection, with a retake flow a human approves. The system flags, a person decides.

**Act four. The day 2,500 candidates arrived at once.**
Peak season, 2,500 concurrent candidates, and the platform started to crawl. The cause was not exotic: N+1 queries, missing indexes, and row-lock contention under load. We rewrote the hot queries, audited the indexes and the locks, and moved the heavy work behind queues. This is still the part of the job I like most, because the feedback is completely unambiguous.

**Act five. The gate that protects the contract.**
Concurrency is what infrastructure costs, and it is what an enterprise client agreement actually pays for. So the assessment platform admits candidates against a configured in-flight limit per platform. Past that limit, a candidate waits for a slot instead of walking into a platform that cannot serve them. Fairness comes from everyone queueing the same way, and the limit is configuration, not a number I get to invent.

Nothing in that list arrived fully formed. It is the standard origin story, the one every shonen arc is built on, except the power-ups are migrations and the training montage is a changelog.

---

## By the numbers

<div align="center">

![Commits](https://img.shields.io/badge/commits-11%2C697-000000?style=flat-square)
![Repositories](https://img.shields.io/badge/repositories-35-000000?style=flat-square)
![Jira](https://img.shields.io/badge/Jira_tickets-1%2C661_at_93%25-000000?style=flat-square)
![Months](https://img.shields.io/badge/active_months-88_of_88-000000?style=flat-square)
![Concurrency](https://img.shields.io/badge/peak_concurrency-2%2C500-000000?style=flat-square)

</div>

Checkable, not rounded up. Every figure traces back to git history or a ticket.

---

## Public code

- **[ShopeeMonitor](https://github.com/anggakersanamunggaran/ShopeeMonitor)** · real-time seller analytics for Shopee: NestJS API and a React dashboard, syncing through the Shopee Open Platform API v2.
- **[laravel-solid-starter](https://github.com/anggakersanamunggaran/laravel-solid-starter)** · a Laravel 12 REST API starting point: slim controllers, a service layer, repository pattern with contracts, typed DTOs, action classes.
- **[Blog-Api](https://github.com/anggakersanamunggaran/Blog-Api)** · architecture study: clean code, onion architecture, dependency injection, Redis Streams.
- **[nest-js-starter-kit](https://github.com/anggakersanamunggaran/nest-js-starter-kit)** · the NestJS setup I reach for.
- **[backend-assessment-python](https://github.com/anggakersanamunggaran/backend-assessment-python)** · a Python backend exercise.

---

## Currently

![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)

Going deep on .NET and C#, deliberately. Seven years across several stacks has given me breadth, and I would rather know one ecosystem properly than keep skimming four. Open to senior full-stack and product engineering work in Bandung or remote.

<div align="center">

**[anggakersana-dev.vercel.app](https://anggakersana-dev.vercel.app)** · **[LinkedIn](https://www.linkedin.com/in/angga-munggaran/)** · **[anggakersana@gmail.com](mailto:anggakersana@gmail.com)**

</div>
