# Hub

The Hub of your community — a platform for neighborhood-scale social infrastructure

## About the Project

Most digital communication platforms treat physical proximity as irrelevant. They optimize for reach, engagement metrics, and network effects that scale to millions. This creates a gap: there's no good infrastructure for the 5-50 people who actually share a street or small neighborhood to coordinate about practical matters—lost pets, shared resources, local decisions, mutual aid.

**Hub** is a platform for hyperlocal communities built on .NET with SQLite. It provides social messaging, threads for longer conversations, ask/offer exchanges, community resource mapping, and proposals for democratic decision-making. Data syncs continuously to a backup location, so if your instance goes down, any community member can spin up a new one from the backup. The system uses proven, simple technology designed for the 5-50 person scale. Data stays within the community, with no corporate intermediary required.

## Core Concepts

### Community Communication
Share updates with your neighbors, start threads for longer discussions, post ask/offer requests for mutual aid, and map community resources. Hub focuses on the practical communication needs of people who share physical space.

### Democratic Governance
Built-in proposal and voting system enables democratic decision-making. Members vote on governance changes, role assignments, and moderation decisions. Vote outcomes are automatically enforced by the system, preventing admin override. Roles (member, moderator, admin) are managed through community governance.

### Simple Backup & Recovery
Data syncs continuously to a backup location (cloud storage or local filesystem). If the primary instance goes down, any community member can restore from the backup and spin up a new instance. No complex distributed systems—just straightforward backup and recovery.

### Community Ownership
Communities own their data and infrastructure. No corporate intermediaries, no centralized servers with access to your conversations. The person running the instance is a community member, accountable through democratic processes.

### Hyperlocal Scale
Built for the 5-50 people who share physical proximity—a street, small neighborhood, or apartment building. The technology choices reflect this scale, favoring simplicity over features designed for millions of users.

## Key Features

- **Social messaging** - Share updates, photos, and links with your community
- **Threads** - Longer-form discussions with nested comments
- **Ask/Offer** - Post requests for help or offer services to neighbors
- **Proposals** - Democratic voting on community decisions
- **Democratic governance** - Role management through community voting
- **Simple backup** - Continuous sync to backup location for easy recovery
- **Community ownership** - No corporate intermediaries, data stays with you
- **Hyperlocal scale** - Optimized for neighborhoods of 5-50 people
- **.NET technology stack** - Built on proven, mature technology (ASP.NET Core, SQLite, Blazor)
- **Rich content** - Markdown formatting, image uploads, file attachments, link previews
- **Docker deployment** - Simple Docker Compose setup with web-based configuration wizard

## How It Works

1. **Deploy with Docker Compose** - Download docker-compose.yml and start containers with one command
2. **Setup Wizard** - Web-based wizard guides initial configuration (community name, admin account, storage)
3. **Start Using Hub** - Share messages, create threads, post ask/offer requests, and create proposals
4. **Continuous Backup** - Database and media continuously sync to a backup location using Litestream
5. **Recovery if Needed** - If your instance goes down, restore from the backup and spin up a new instance
6. **Democratic Operations** - Members vote on governance changes through the built-in proposal system

Communities start with a simple Docker deployment. The setup wizard handles initial configuration. The initial operator becomes the first admin. Over time, communities can elect additional admins through the proposal system.

## Project Status

**Current Phase**: Concept Development (January 2026)

We are in the early planning stages, defining architecture decisions and exploring technical approaches for community features and democratic governance mechanisms.

## Documentation

- [Documentation](docs/README.md) - Project documentation overview
- [Architecture Decision Records](docs/adrs/README.md) - Key technical and governance decisions that define the platform

## Code Repository

This repository contains the planning documentation and will eventually house the implementation.

## Getting Involved

This project is in early development. If you're interested in:

- **Contributing to design** - Review [Architecture Decision Records](docs/adrs/README.md) and provide feedback
- **Technical development** - Watch this repo for implementation opportunities
- **Starting a neighborhood** - Follow the project as deployment documentation develops

## License

This project is licensed under the [GNU General Public License v3.0](LICENSE).

The GPL v3 ensures that this infrastructure remains free and open. Communities have the freedom to run, study, modify, and distribute the software. Any modifications must also be released under GPL v3, preventing proprietary capture of community infrastructure.
