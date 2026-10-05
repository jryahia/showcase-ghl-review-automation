# GHL Review Automation

**Review-request automation for GoHighLevel: a completed job triggers a Google, Facebook or Yelp review request with smart follow-up. Sending is simulated in this version.**

> **This is a proprietary project. Source code is private. This page showcases the system's architecture and results.**

**Case study page:** [https://jryahia.github.io/showcase-ghl-review-automation/](https://jryahia.github.io/showcase-ghl-review-automation/)

![GHL Review Automation](assets/00-dashboard.png)

## Problem it solves

Happy customers rarely leave reviews unless asked at the right moment. This system sends the request automatically when GoHighLevel marks a job complete, follows up if there is no response, and tracks the outcome.

## Architecture

![Architecture](assets/architecture.svg)

1. GoHighLevel signals a completed job.
2. A review request is created for the chosen platform and sent from a template.
3. If there is no action, reminders go out up to a configured limit.
4. Request status moves from pending to sent, opened, and submitted or declined.

## Key features

- Google, Facebook and Yelp review links
- Template system with placeholders
- Configurable follow-up delay and count
- Lifecycle tracking per request
- Dashboard with activity feed

## Tech stack

![Python](https://img.shields.io/badge/Python-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![FastAPI](https://img.shields.io/badge/FastAPI-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![GoHighLevel API](https://img.shields.io/badge/GoHighLevel%20API-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![Jinja2](https://img.shields.io/badge/Jinja2-161b22?style=for-the-badge&labelColor=161b22&color=161b22)

## What it does in practice

- Prototype stage: the request lifecycle, templates and follow-up scheduling are built; SMS/email sending is simulated (Twilio/SendGrid hookup is the next step).

## Screenshots

> Screenshots show the app running on seeded demo data, not client data.

**Requests by platform and status**

![Requests by platform and status](assets/00-dashboard.png)

**API surface: webhooks, requests, templates, follow-ups**

![API surface: webhooks, requests, templates, follow-ups](assets/10-api.png)

---

Built by [Yahya Jarray](https://github.com/jryahia). Interested in a similar system? [Get in touch](mailto:yahiajarray43@gmail.com).

This repository contains no source code. It is a case study for a proprietary project. © Yahya Jarray.
