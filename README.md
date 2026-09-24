<div align="center">

# Angga Kersana Munggaran

**Senior full-stack engineer · backend-leaning**

Seven years building hiring software at ASTRNT, from the product spec through to production and the incident calls in between.

[![Portfolio](https://img.shields.io/badge/anggakersana--dev.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://anggakersana-dev.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/angga-munggaran/)
[![Email](https://img.shields.io/badge/anggakersana@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:anggakersana@gmail.com)

</div>

---

**Hi. You are on my GitHub, which usually means one of three things: you are hiring, you are a developer who followed my name here from somewhere, or you are me at 2am checking whether the push actually went through. All three of you are welcome.**

I am Angga, a backend-leaning full-stack engineer based in Indonesia. Seven years of my career went into one product family: hiring software at ASTRNT, built for enterprise clients who hire in serious volume.

People ask what a backend engineer actually does all day. The honest answer is the two hard problems in computer science: cache invalidation and naming things. And off-by-one errors.

Engineering has three moods, and I have had all of them this month: it works on my machine, it works in production and nobody knows why, and it stopped working and nobody touched it. The third one is where I have learned nearly everything I know. I am also the person who asks what happens if the connection drops halfway through, because it always does eventually.

The job title sounds grander than the actual work. Most of my days are writing the specification, building the thing, and then staying around for the call when it breaks in production. Shipping to production has a lot in common with UDP: you do find out whether it arrived, just never at a convenient time.

The part people seem to remember about working with me is that I am good company in a long week. I will take that over most compliments.

**A few ways in:**
- [What I have shipped](#what-i-have-shipped) if you want the stories rather than the list.
- [Public code](#public-code) if you would rather read code than prose.
- [anggakersana@gmail.com](mailto:anggakersana@gmail.com) if you want to talk about a role. I answer.

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

Seven years on one product family: HR technology for enterprise clients, sold as B2B SaaS. Every story below starts with a sentence nobody wants to hear in a planning meeting, usually "can we just" followed by a request that is secretly three requests. Five of them, each with a setup and a punchline, because that is honestly the shape they have.

**Act one. The scheduling problem.**
Hiring at volume used to run on interviewer calendars. A recruiter opens the calendar, sees forty free slots, books forty interviews, and congratulations, you have just employed a human being as a scheduling algorithm.

So we built asynchronous video interviews with automatic scoring and a transcript summary. The candidate answers on their own clock, and screening capacity stops depending on how many interviewers remembered to block their lunch hour.

**Act two. The candidate who lost their answer.**
You know this one. The progress bar reaches ninety-nine percent, the spinner starts reconsidering its life choices, and then the browser decides it has done enough for today. In most apps that is a mild inconvenience. In an interview it costs a candidate the entire attempt, and there is no version of that conversation where the candidate is at fault.

So the upload became a chunked path with server-side reconstruction. The pieces land as they are sent, the server rebuilds the file, and a bad connection now costs seconds instead of an interview. The progress bar still lies to you, it just lies faster. The proctoring audio stream, the part with no package behind it, is the one I wrote myself.

**Act three. The recording nobody could score.**
The mute button is the most powerful button in human history. A silent or frozen recording used to arrive at a reviewer looking exactly like a completed answer, which means the platform quietly fails a good candidate for the crime of owning a cheap headset.

So we put a quality gate in front of it, using ffmpeg silence and freeze detection. The system flags, a human decides, and the retake flow exists because a machine should never get the last word on whether a person gets a job.

**Act four. The day 2,500 candidates arrived at once.**
It worked on my machine. It worked on your machine. It worked on the staging server that has seen things. Then peak season arrived, 2,500 concurrent candidates, and the platform started to crawl in a way that felt deliberate.

The cause was not exotic: N+1 queries, missing indexes, row-lock contention. One innocent query quietly turning into two thousand five hundred queries is the database equivalent of one person asking a question and the whole room answering at once. We rewrote the hot queries, audited the indexes and the locks, and moved the heavy work behind queues. Still my favourite kind of day, because the feedback is completely unambiguous.

**Act five. The gate that protects the contract.**
Concurrency is what infrastructure costs, and it is what an enterprise client agreement actually pays for. Let everyone in at once and the invoice and the experience both fall over.

So we built the thing everybody hates and everybody needs: a queue. Past the configured in-flight limit, a candidate waits for a slot instead of walking into a platform that cannot serve them. The difference between our queue and the one at the bank is that ours tells you why you are waiting. Fairness comes from everyone queueing the same way, and the limit is configuration, not a number I get to invent.

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

Everything above was the packaging. This part drops the act: checkable, not rounded up, and every figure traces back to git history or a ticket.

---

## Public code

Five repositories that show how I build, rather than everything I have ever pushed. Each one runs with Docker, and the two that carry real invariants have tests.

**[laravel-solid-starter](https://github.com/anggakersanamunggaran/laravel-solid-starter)**
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white)
The layering I reach for in a new backend: slim controllers, a real service layer, repositories behind contracts, typed DTOs, and one action class per mutation. A starter without Docker and tests is just a folder.

**[nest-js-starter-kit](https://github.com/anggakersanamunggaran/nest-js-starter-kit)**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
The same architecture in a second stack, on purpose: identical read and write separation, idiomatic NestJS. Worth a look if you want to know the philosophy is not just a Laravel habit.

**[ShopeeMonitor](https://github.com/anggakersanamunggaran/ShopeeMonitor)**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
A product rather than a demo: a NestJS API and a React dashboard that sync seller orders and escrow data through the Shopee Open Platform API v2, then work out net profit per SKU. TypeORM, Redis, BullMQ for the sync jobs, and rate limiting so the upstream API stays happy.

**[ottodot-takehome](https://github.com/anggakersanamunggaran/ottodot-takehome)**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
The smallest working slice of a booking system that has to stay correct under concurrency and payment failure, which is usually the part an exercise like this skips. Schema, invariants and tests included.

**[backend-assessment-python](https://github.com/anggakersanamunggaran/backend-assessment-python)**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
A customer data pipeline: a Flask mock source, a FastAPI ingest service using dlt, PostgreSQL, and a REST API in front of it, all containerised and laid out in Onion Architecture.

---

## Currently

![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)

Going deep on .NET and C#, deliberately. Seven years across several stacks has given me breadth, and I would rather know one ecosystem properly than keep skimming four. Open to senior full-stack and product engineering work in Bandung or remote.

<div align="center">

**[anggakersana-dev.vercel.app](https://anggakersana-dev.vercel.app)** · **[LinkedIn](https://www.linkedin.com/in/angga-munggaran/)** · **[anggakersana@gmail.com](mailto:anggakersana@gmail.com)**

</div>
