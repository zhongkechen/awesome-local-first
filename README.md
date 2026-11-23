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

- [Earthstar](https://github.com/earthstar-project/earthstar) - Decentralized local-first storage and synchronization protocol with offline operation, multi-device replication, and verifiable deletion. Open-source (LGPL-3.0).
- [Iroh](https://github.com/n0-computer/iroh) - Peer-to-peer networking and content-addressed data synchronization stack (`iroh-blobs`, `iroh-docs`) for building local-first applications. Open-source (Apache-2.0 / MIT).
- [Keyhive](https://github.com/inkandswitch/keyhive) - Decentralized local-first access control and encrypted capabilities protocol from Ink & Switch, designed for CRDT and causal-graph synchronization. Open-source (Apache-2.0); pre-alpha.
- [Secure Scuttlebutt](https://scuttlebutt.nz/) - A peer-to-peer protocol for local-first applications, using signed append-only feeds with offline operation and decentralized replication.
- [Willow](https://willowprotocol.org/) - Family of peer-to-peer data storage and synchronization protocols for local-first software, featuring range-based set reconciliation, fine-grained capabilities, and true deletion.

## Libraries

- [automerge](https://github.com/automerge/automerge) - A JSON-like data structure (a CRDT) that can be modified concurrently by different users, and merged again automatically.
- [cr-sqlite](https://github.com/vlcn-io/cr-sqlite) - A SQLite extension that adds CRDT-backed tables for local-first applications.
- [DXOS](https://github.com/dxos/dxos) - Local-first application framework built around ECHO, a peer-to-peer CRDT database for offline-capable web apps. Source-available (FSL-1.1-Apache-2.0).
- [ElectricSQL](https://github.com/electric-sql/electric) - A sync engine for building local-first apps on top of Postgres.
- [Evolu](https://github.com/evoluhq/evolu) - Local-first, end-to-end encrypted SQLite database and CRDT sync platform for web, React Native, and Electron apps. Open-source (MIT).
- [Fireproof](https://github.com/fireproof-storage/fireproof) - Embedded local-first Merkle CRDT document database for browsers and edge environments with encrypted multi-device sync. Open-source (Apache-2.0 / MIT).
- [hypercore](https://github.com/hypercore-protocol/hypercore) - Hypercore is a secure, distributed append-only log.
- [Jazz](https://github.com/garden-co/jazz) - An open-source framework for building local-first apps with sync, permissions, and account handling.
- [LiveStore](https://github.com/livestorejs/livestore) - A local-first data layer for web apps with reactive queries and sync.
- [Loro](https://github.com/loro-dev/loro) - High-performance CRDT library in Rust with WASM, JS, Swift, and Python bindings, supporting rich text, movable trees, and time-travel version history. Open-source (MIT).
- [PouchDB](https://github.com/pouchdb/pouchdb) - A JavaScript database that runs in the browser and syncs with CouchDB-compatible servers.
- [PowerSync](https://github.com/powersync-ja/powersync-js) - Open-source (Apache-2.0) sync engine that keeps local SQLite databases in sync with Postgres, MongoDB, or MySQL backends across web, mobile, and desktop, with self-hosted or managed PowerSync Service options.
- [Replicache](https://replicache.dev/) - A sync framework for building low-latency, collaborative web apps with local optimistic updates.
- [RxDB](https://github.com/pubkey/rxdb) - A local-first JavaScript database with replication support for browsers, Node.js, and mobile apps.
- [selfstore](https://github.com/selfstoredev/selfstore) - Local-first storage for browser apps: an IndexedDB working copy, portable, optionally encrypted ZIP backups, and durable homes on disk, Google Drive, WebDAV or S3.
- [TinyBase](https://github.com/tinyplex/tinybase) - A reactive local data store for building local-first web apps, with persistence and synchronization options.
- [Triplit](https://www.triplit.dev/) - A syncing database for local-first web apps with optimistic updates, subscriptions, and schema support.
- [WatermelonDB](https://github.com/Nozbe/WatermelonDB) - Reactive local SQLite database for React Native and web apps with built-in incremental sync primitives. Open-source (MIT).
- [Yjs](https://github.com/yjs/yjs) - A high-performance CRDT framework for building collaborative local-first applications.
- [Yrs](https://github.com/y-crdt/y-crdt) - Rust port of the Yjs CRDT framework with bindings for Python, Swift, and WebAssembly. Open-source (MIT).
- [Zero](https://github.com/rocicorp/mono) - General-purpose local-first sync engine for web apps from the makers of Replicache, providing instant local queries synchronized with a backend database. Open-source (Apache-2.0).

## Applications

### Developer Tools

- [git-bug](https://github.com/git-bug/git-bug) - Distributed, offline-first bug tracker that embeds issues and comments as operation DAGs inside Git objects and syncs over standard Git remotes. Open-source (GPL-3.0).
- [Hyperconsciousness](https://github.com/louis030195/hyperconsciousness) - Local-first, encrypted, append-only knowledge store in Rust with device sync and CLI/MCP access through scoped, expiring grants. Developer alpha.
- [Radicle](https://radicle.xyz/) - Peer-to-peer code collaboration stack built on Git and gossip replication; works offline with CRDT-backed Collaborative Objects (COBs) for issues and patches. Open-source (MIT / Apache-2.0).

### Knowledge Management

- [Anytype](https://github.com/anyproto/anytype-ts) - Local-first, encrypted, peer-to-peer workspace for notes, tasks, documents, and personal knowledge.
- [AppFlowy](https://github.com/AppFlowy-IO/AppFlowy) - Open-source (AGPL-3.0) local-first workspace built with Rust, Flutter, and Yrs CRDTs. Supports offline local mode, Markdown/JSON export, and optional self-hosted or hosted AppFlowy Cloud sync and AI features.
- [BINGO!](https://github.com/MingYiShang/BINGO) - Open-source (MIT) local-first workspace combining a Markdown editor, Bento grids, edgeless canvas, MECE trees, and a 3D knowledge graph. Notes are stored as local plain-text `.md` files with zero telemetry, optional user-configured WebDAV/LAN sync and BYO-key external AI proxies, or a strict `--air-gapped` mode that disables all network and LAN handlers.
- [Joplin](https://github.com/laurent22/joplin) - Open-source (AGPL-3.0) offline-first Markdown note-taking and to-do app using local SQLite storage, JEX/Markdown export, and optional end-to-end encrypted sync via WebDAV, Nextcloud, S3, Dropbox, OneDrive, or Joplin Cloud.
- [Koru](https://github.com/koruworks/mono) - Open-source, local-first Rust workspace for notes, docs, and files. Notes stay in a local database and sync peer-to-peer with no account by default; official builds can optionally sign in to Koru Cloud, and usage telemetry is opt-in.
- [Logseq](https://github.com/logseq/logseq) - Local-first outliner and knowledge base built around local Markdown and Org-mode files.
- [NextGraph](https://github.com/nextgraph-org/nextgraph-rs) - Open-source (Apache-2.0 / MIT) decentralized, end-to-end encrypted local-first workspace built on CRDTs for offline editing and peer-to-peer or broker-assisted multi-device sync.
- [NoteGen](https://github.com/codexu/note-gen) - Open-source local-first Markdown note-taking app that stores written notes as ordinary files and supports optional user-controlled sync.
- [Notesnook](https://github.com/streetwriters/notesnook) - Open-source (GPL-3.0) offline-first, end-to-end encrypted note-taking app with local storage, Markdown/HTML/PDF and encrypted backup export, and optional cloud sync.
- [Obsidian](https://obsidian.md/) - Local-first Markdown knowledge base with local files and optional paid sync.
- [Screenpipe](https://github.com/screenpipe/screenpipe) - Searchable screen and audio history for recall, meeting notes, and work summaries, accessible through a local API and MCP. Raw history stays on-device by default; configured cloud AI, transcription, sync, and integrations can transmit context off-device. Source-available under the Screenpipe Commercial License.
- [SiYuan](https://github.com/siyuan-note/siyuan) - Open-source (AGPL-3.0) offline-first personal knowledge management system storing notes as local JSON and Markdown, with full export and optional end-to-end encrypted sync via S3, WebDAV, or SiYuan Cloud.
- [Standard Notes](https://github.com/standardnotes/app) - Open-source (AGPL-3.0) offline-first, end-to-end encrypted note-taking app with plaintext and encrypted backup exports and optional sync via hosted or self-hosted servers.
- [TriliumNext](https://github.com/TriliumNext/Trilium) - Open-source (AGPL-3.0) hierarchical note-taking app backed by local SQLite with Markdown/HTML/OPML export and built-in multi-device sync via a self-hosted sync server.

### Productivity

- [AFFiNE](https://github.com/toeverything/AFFiNE) - Local-first workspace for documents, whiteboards, and knowledge management.
- [Anki](https://github.com/ankitects/anki) - Open-source (AGPL-3.0) offline-first spaced-repetition flashcard app backed by local SQLite, with `.apkg`/`.colpkg` backup exports and optional multi-device sync via AnkiWeb or a self-hosted sync server.
- [Orkas](https://github.com/Orkas-AI/Orkas) - Open-source, local-first desktop AI workforce that stores conversations, files, agent configuration, and model credentials locally. Prompts and selected file content are sent directly to the configured model provider, and hosted builds may support cloud sync.
- [Super Productivity](https://github.com/super-productivity/super-productivity) - Open-source (MIT) offline-first task manager and time tracker with local storage, JSON backup/export, and optional multi-device sync via WebDAV, Dropbox, Nextcloud, or local file sync.
- [Tasks.org](https://github.com/tasks/tasks) - Open-source (GPL-3.0) offline-first Android task manager with local storage, JSON backup/export, and optional sync via CalDAV, DAVx5, EteSync, DecSync, or paid Tasks.org Cloud.

### Communication

- [Delta Chat](https://delta.chat/) - Open-source (MPL-2.0) decentralized, offline-first, end-to-end encrypted messaging app using local SQLite storage, encrypted backup transfer, and multi-device sync over email/chatmail servers.
- [Quiet](https://github.com/TryQuiet/quiet) - Open-source (GPL-3.0) peer-to-peer team chat built on Tor and OrbitDB/CRDTs with no central server, offline message composition, and automatic multi-device sync when online.

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
