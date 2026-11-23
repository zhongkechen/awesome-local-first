# awesome-local-first

A curated list of awesome [Local-First Software](https://www.inkandswitch.com/local-first/)

## Introduction

What is local first?

- [Local-first software - You own your data, in spite of the cloud](https://www.inkandswitch.com/local-first/)
  - [PDF Version](https://martin.kleppmann.com/papers/local-first.pdf)
- [Automerge: Making servers optional for real-time collaboration - Martin Kleppmann](https://www.youtube.com/watch?v=PHz17gwiOc8)
- [Verifying strong eventual consistency in distributed systems](https://dl.acm.org/doi/10.1145/3133933)

## Inclusion criteria

This list focuses on **local-first** software—not purely local-only apps or one-off client-side utilities.

Applications must keep the primary copy of their core user data on the user's device and meet all three requirements:

- **Continue offline.** After setup, users can reopen saved work offline to edit documents or projects, manage records, or browse or recover archived data. For web apps, this means working offline across reloads (such as a cached PWA), not just keeping an open tab.
- **Keep an independent copy.** Users can back up or move that data without the vendor's service, using files they control, a documented reusable export, or a restorable backup.
- **Built for sync or collaboration.** Applications must support multi-device synchronization or collaboration (such as peer-to-peer, user-controlled/self-hosted sync, or optional cloud sync), **or** build their local store on data structures specifically designed for synchronization and conflict-free merging (such as CRDTs, hybrid logical clocks, or signed append-only logs).

Out of scope for the application list:

- Purely local-only applications without multi-device sync or sync-oriented data structures (relying solely on a third-party folder sync tool without sync-oriented data structures is insufficient).
- Tools whose workflow ends after a one-off conversion, compression, or export (remembered processing settings and cached inputs alone are insufficient).
- General local file viewers or system utilities whose only local state is app configuration.
- Waitlist-only or unreleased projects. (Early-access or alpha software is allowed if labeled as such.)

An application can qualify through a supported local mode or edition (such as local AI models or an offline-only mode). Identify that mode and disclose all network behavior, including cloud features, accounts, telemetry/analytics, update or license checks, and initial model downloads.

Libraries and protocols should directly support building local-first applications through capabilities such as on-device persistence, replication, synchronization, or conflict resolution.

See [CONTRIBUTING.md](CONTRIBUTING.md) for full inclusion criteria, licensing and disclosure rules, and submission guidelines.

## Protocols

- [Secure Scuttlebutt](https://scuttlebutt.nz/) - A peer-to-peer protocol for local-first applications, using signed append-only feeds with offline operation and decentralized replication.

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

- [Hyperconsciousness](https://github.com/louis030195/hyperconsciousness) - Local-first, encrypted, append-only knowledge store in Rust with device sync and CLI/MCP access through scoped, expiring grants. Developer alpha.

### Knowledge Management

- [Anytype](https://github.com/anyproto/anytype-ts) - Local-first, encrypted, peer-to-peer workspace for notes, tasks, documents, and personal knowledge.
- [Koru](https://github.com/koruworks/mono) - Open-source, local-first Rust workspace for notes, docs, and files. Notes stay in a local database and sync peer-to-peer with no account by default; official builds can optionally sign in to Koru Cloud, and usage telemetry is opt-in.
- [Logseq](https://github.com/logseq/logseq) - Local-first outliner and knowledge base built around local Markdown and Org-mode files.
- [NoteGen](https://github.com/codexu/note-gen) - Open-source local-first Markdown note-taking app that stores written notes as ordinary files and supports optional user-controlled sync.
- [Obsidian](https://obsidian.md/) - Local-first Markdown knowledge base with local files and optional paid sync.
- [Screenpipe](https://github.com/screenpipe/screenpipe) - Searchable screen and audio history for recall, meeting notes, and work summaries, accessible through a local API and MCP. Raw history stays on-device by default; configured cloud AI, transcription, sync, and integrations can transmit context off-device. Source-available under the Screenpipe Commercial License.

### Productivity

- [AFFiNE](https://github.com/toeverything/AFFiNE) - Local-first workspace for documents, whiteboards, and knowledge management.
- [Orkas](https://github.com/Orkas-AI/Orkas) - Open-source, local-first desktop AI workforce that stores conversations, files, agent configuration, and model credentials locally. Prompts and selected file content are sent directly to the configured model provider, and hosted builds may support cloud sync.

### Social Networks

- [Oasis](https://github.com/epsylon/oasis) - Self-hosted community application for blogs, documents, and collaborative pads, backed by an on-disk SSB database and peer-to-peer replication; uses the separate Oasis network by default.
- [Tilde Friends](https://dev.tildefriends.net/cory/tildefriends) - Cross-platform SSB social client and web app platform for posts, messages, and user-created apps; local installations support on-device storage, offline use, and peer-to-peer synchronization.

### Finance

- [Actual](https://github.com/actualbudget/actual) - Local-first personal finance app with optional sync and end-to-end encrypted budget data.

### Retail & Commerce

- [Posnic](https://github.com/Posnic/POS) - Free, open-source POS and Billing Software for retail shops and restaurants. Primary data stays on the till for offline checkout, with optional self-hosting for Online/Offline POS workflows. [Website](https://www.posnic.com/)
