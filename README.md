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
- [selfstore](https://github.com/selfstoredev/selfstore) - Local-first storage for browser apps: an IndexedDB working copy, portable, optionally encrypted ZIP backups, and durable homes on disk, Google Drive, WebDAV or S3.
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

### Bookmarks & Browser Sync

- [Floccus](https://github.com/floccusaddon/floccus) - Open-source (MPL-2.0) cross-browser bookmark and tab sync extension keeping local browser bookmarks as the primary copy, with export and user-controlled sync via WebDAV, Nextcloud, Git, or Google Drive.

### Design & Spatial Canvases

- [Muse](https://museapp.com/) - Proprietary offline-first spatial thinking canvas for Mac and iPad with local-first document storage, export options, and optional multi-device sync and collaboration.

### File Sync & Storage

- [git-annex](https://git-annex.branchable.com/) - Open-source (AGPL-3.0) distributed file management and multi-device synchronization tool built on Git, keeping primary file copies under user control across offline and online devices.
- [Syncthing](https://github.com/syncthing/syncthing) - Open-source (MPL-2.0) decentralized peer-to-peer continuous file synchronization application with no central server, keeping primary copies on each user's devices.

### Maps, GIS & Field Data

- [CoMapeo](https://comapeo.app/) - Open-source (GPL-3.0) offline-first mapping and field documentation app built on peer-to-peer sync (Hypercore) for collecting and synchronizing geospatial records over local Wi-Fi without internet access.
- [Mergin Maps](https://github.com/MerginMaps/mobile) - Open-source (GPL-2.0) offline-first mobile GIS field data collection app backed by local GeoPackage files with diff-based (GeoDiff) multi-device synchronization via hosted or self-hosted servers.
- [QField](https://github.com/opengisch/QField) - Open-source (GPL-2.0) offline-first mobile GIS app built on QGIS, storing projects locally in GeoPackage files with incremental sync via QFieldCloud or user-managed storage.

### Passwords & Secrets

- [Gopass](https://github.com/gopasspw/gopass) - Open-source (MIT) team-capable local-first password manager storing GPG- or age-encrypted secrets as local files synchronized through Git.
- [Keepass2Android](https://github.com/PhilippC/keepass2android) - Open-source (GPL-3.0) offline-first Android password manager for standard `.kdbx` vaults, featuring built-in WebDAV, SFTP, or cloud sync with three-way conflict merging.
- [Pass](https://www.passwordstore.org/) - Open-source (GPL-2.0) Unix password manager storing each secret in a GPG-encrypted local file inside a Git repository for offline access and multi-device synchronization.

### Personal Tracking & Journaling

- [Lotti](https://github.com/matthiasn/lotti) - Open-source (GPL-3.0) local-first personal tracking, journaling, and task app backed by local SQLite, vector clocks, and end-to-end encrypted multi-device sync over Matrix with no vendor cloud or account.

### Research, Reading & Media

- [AntennaPod](https://github.com/AntennaPod/AntennaPod) - Open-source (GPL-3.0) offline-first Android podcast player backed by local SQLite, with OPML and full database backups plus optional multi-device sync via gpodder.net or Nextcloud.
- [KOReader](https://github.com/koreader/koreader) - Open-source (AGPL-3.0) offline-first e-book reader for e-ink and mobile devices with local book and annotation storage/exports, plus built-in reading progress sync via kosync or a self-hosted sync server.
- [NetNewsWire](https://github.com/Ranchero-Software/NetNewsWire) - Open-source (MIT) offline-first RSS feed reader backed by local SQLite with OPML export and optional multi-device sync via iCloud, FreshRSS, Feedbin, or compatible services.
- [Zotero](https://github.com/zotero/zotero) - Open-source (AGPL-3.0) offline-first reference and research manager backed by local SQLite, with BibTeX/RIS/CSL and library export plus optional multi-device sync via Zotero Sync or WebDAV.
