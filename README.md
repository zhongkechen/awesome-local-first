# awesome-local-first

A curated list of awesome [Local-First Software](https://www.inkandswitch.com/local-first/)

## Introduction

What is local first?

- [Local-first software - You own your data, in spite of the cloud](https://www.inkandswitch.com/local-first/)
  - [PDF Version](https://martin.kleppmann.com/papers/local-first.pdf)
- [Automerge: Making servers optional for real-time collaboration - Martin Kleppmann](https://www.youtube.com/watch?v=PHz17gwiOc8)
- [Verifying strong eventual consistency in distributed systems](https://dl.acm.org/doi/10.1145/3133933)

## Libraries

- [automerge](https://github.com/automerge/automerge) - A JSON-like data structure (a CRDT) that can be modified concurrently by different users, and merged again automatically.
- [cr-sqlite](https://github.com/vlcn-io/cr-sqlite) - A SQLite extension that adds CRDT-backed tables for local-first applications.
- [ElectricSQL](https://github.com/electric-sql/electric) - A sync engine for building local-first apps on top of Postgres.
- [hypercore](https://github.com/hypercore-protocol/hypercore) - Hypercore is a secure, distributed append-only log.
- [Jazz](https://github.com/garden-co/jazz) - An open-source framework for building local-first apps with sync, permissions, and account handling.
- [LiveStore](https://github.com/livestorejs/livestore) - A local-first data layer for web apps with reactive queries and sync.
- [PouchDB](https://github.com/pouchdb/pouchdb) - A JavaScript database that runs in the browser and syncs with CouchDB-compatible servers.
- [Replicache](https://replicache.dev/) - A sync framework for building low-latency, collaborative web apps with local optimistic updates.
- [RxDB](https://github.com/pubkey/rxdb) - A local-first JavaScript database with replication support for browsers, Node.js, and mobile apps.
- [TinyBase](https://github.com/tinyplex/tinybase) - A reactive local data store for building local-first web apps, with persistence and synchronization options.
- [Triplit](https://www.triplit.dev/) - A syncing database for local-first web apps with optimistic updates, subscriptions, and schema support.
- [Yjs](https://github.com/yjs/yjs) - A high-performance CRDT framework for building collaborative local-first applications.

## Applications

### Developer Tools

- [Luminy](https://github.com/luminy-agent/desktop) - Local-first desktop AI coding assistant that stores sessions, project data, settings, API keys, and code indexes locally, with offline Ollama support and optional cloud AI providers.
- [Tree Ring Memory](https://github.com/TerminallyLazy/Tree-Ring-Memory) - Local-first, SQLite/FTS-backed memory lifecycle CLI/TUI for AI agents with explicit recall, redaction, deletion, audit, consolidation, and JSON export.

### Knowledge Management

- [Anytype](https://github.com/anyproto/anytype-ts) - Local-first, encrypted, peer-to-peer workspace for notes, tasks, documents, and personal knowledge.
- [Logseq](https://github.com/logseq/logseq) - Local-first outliner and knowledge base built around local Markdown and Org-mode files.
- [Obsidian](https://obsidian.md/) - Local-first Markdown knowledge base with local files and optional paid sync.

### Productivity

- [AFFiNE](https://github.com/toeverything/AFFiNE) - Local-first workspace for documents, whiteboards, and knowledge management.

### Social Networks

- [Secure Scuttlebutt](https://scuttlebutt.nz/) - a peer-to peer communication protocol, mesh network, and self-hosted social media ecosystem

### Finance

- [Actual](https://github.com/actualbudget/actual) - Local-first personal finance app with optional sync and end-to-end encrypted budget data.
- [FreeFile ITR](https://github.com/rohitthink/freefile) - A privacy-first income tax return filing app for Indian freelancers. Imports bank statements, computes tax under both old and new regimes, and files directly on incometax.gov.in. All financial data is stored locally on the user's device using SQLite. Built with Next.js, FastAPI, and Tauri. Licensed under AGPL-3.0.
