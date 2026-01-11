# Hub

**The digital hub of your neighborhood**

## Overview

Hub is a platform for hyperlocal community infrastructure, built for the 5-50 people who share a street, apartment building, or small neighborhood. It fills a gap that mainstream social platforms ignore: practical coordination for people who actually know each other and share physical space.

## The Problem

Most digital communication platforms treat physical proximity as irrelevant. They optimize for reach, engagement metrics, and network effects that scale to millions. This leaves neighborhoods without good infrastructure for the things that actually matter locally: coordinating about lost pets, sharing tools, making collective decisions, and helping each other out.

Existing solutions either require corporate intermediaries (Nextdoor, Facebook Groups) or aren't designed for the intimate scale of real neighborhoods. Hub is different.

## What Hub Provides

### Community Communication

- **Social messaging** - Share updates, photos, and links with your neighbors
- **Threaded discussions** - Longer conversations with nested comments
- **Ask/Offer exchanges** - Post requests for help or offer services ("Need a ladder this weekend" / "Free tomatoes from my garden")
- **Rich content** - Markdown formatting, image uploads, file attachments, and link previews

### Democratic Governance

Hub treats governance as infrastructure, not an afterthought.

- **Proposal system** - Any member can create proposals for community decisions
- **Transparent voting** - Configurable voting rules, duration, and thresholds
- **Automated enforcement** - When the community votes to add or remove a moderator, the system makes it happen automatically. Admins cannot override democratic decisions.
- **Role management** - Member, Moderator, and Admin roles are managed through community voting, not top-down appointment

### Community Ownership

- **Your data stays with you** - No corporate intermediaries with access to your conversations
- **No external dependencies** - Works in isolated networks or when internet infrastructure is unavailable
- **Continuous backup** - Data syncs automatically to a backup location. If your instance goes down, any trusted community member can spin up a new one from the backup.
- **GPL v3 licensed** - The code is free and open. Any modifications must also remain open source.

## Design Philosophy

### Built for Neighborhood Scale

Hub is deliberately designed for 5-50 users, not millions. This shapes every technical decision:

- Simple backup and recovery instead of complex distributed systems
- Manual failover is acceptable (and even desirable for community involvement)
- Members know each other, which changes how identity verification and password recovery work
- Admin-assisted account recovery leverages the fact that you can verify identity in person

### Resilience Without Complexity

The backup model is simple: data continuously syncs to a backup location. If the primary instance goes down, restore from backup and spin up a new one. No complex clustering, no consensus protocols, no split-brain scenarios to debug at 2am.

This simplicity is a feature. Post-disaster scenarios, isolated networks, or situations where the original operator is unavailable are all handled by the same straightforward recovery process.

### Democratic Infrastructure

Technical systems enforce democratic outcomes. When a proposal passes, the result is applied automatically. The person running the server is a community member accountable through the same governance processes as everyone else, not an all-powerful administrator.

## Key Features at a Glance

| Feature | Description |
|---------|-------------|
| Social Messaging | Share updates, photos, and links with your community |
| Threads | Longer discussions with nested comments |
| Ask/Offer | Mutual aid posts for requesting and offering help |
| Proposals | Democratic voting on community decisions |
| Invite System | Controlled membership growth through invite codes |
| Continuous Backup | Automatic sync to backup location for disaster recovery |
| Docker Deployment | Simple setup with web-based configuration wizard |
| No Corporate Dependencies | Works offline, in isolated networks, or post-disaster |

## Technology

Hub is built on proven, mature technology:

- **.NET** with SQLite for a simple, portable data layer
- **Litestream** for continuous database backup to cloud storage or local filesystem
- **Docker Compose** for straightforward deployment
- Web-based setup wizard for initial configuration

The technology choices prioritize simplicity and long-term maintainability over cutting-edge features.

## Project Status

Hub is currently in concept development (January 2026). Architecture decisions have been documented and implementation planning is underway.

## License

GNU General Public License v3.0 - ensuring community infrastructure remains free and open.
