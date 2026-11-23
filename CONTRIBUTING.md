# Contributing to awesome-local-first

Thank you for contributing to `awesome-local-first`. This list curates **local-first** protocols, libraries, and applications grounded in the principles of [Local-First Software](https://www.inkandswitch.com/local-first/).

## Inclusion criteria

### Applications

An application must keep the primary copy of its core user data on the user's device and satisfy **all three** of the following requirements:

1. **Continue offline.** After initial setup, users can reopen saved work offline to edit documents or projects, manage records, or browse or recover archived data.
   - For web apps, this means working offline across reloads (for example, as a cached PWA), not merely keeping an already-loaded browser tab open.
2. **Keep an independent copy.** Users can back up or move their data without relying on the vendor's service—using ordinary files they control, a documented reusable export format, or a restorable backup.
3. **Built for multi-device sync or collaboration.** Applications must either:
   - Support multi-device synchronization or collaboration (such as peer-to-peer sync, user-controlled/self-hosted sync, or optional cloud sync), **or**
   - Build their local data store on data structures specifically designed for synchronization and conflict-free merging (such as CRDTs, hybrid logical clocks, Merkle DAGs, or signed append-only logs).

#### Supported local modes and AI applications

An application can qualify through a supported local mode or edition (for example, an offline-only mode or local AI models via Ollama, MLX, or ONNX). In that mode, the core workflow must remain usable offline (or allow full offline access, editing, and export of saved work). Clearly identify the local mode and disclose what leaves the device when optional cloud features or cloud models are enabled.

#### Out of scope for applications

- **Purely local-only apps** with neither multi-device sync nor sync-oriented data structures (merely saving files into a user-chosen folder for third-party file sync, without sync-oriented data structures or built-in sync, is insufficient).
- **One-off utilities** whose workflow ends after a single conversion, compression, or export. Remembered processing settings and cached inputs alone do not qualify.
- **General local file viewers or system utilities** whose only persistent local state is application preferences or OS configuration.
- **Waitlist-only or unreleased projects.** Projects must be publicly usable today. Early-access, beta, or alpha software is allowed if labeled clearly in the entry.

### Libraries and protocols

Libraries and protocols should directly support building local-first applications through capabilities such as on-device persistence, replication, synchronization, or conflict resolution.

## Disclosure and accuracy requirements

- **Licensing:**
  - Label proprietary apps explicitly as `Proprietary` (and note free/paid tiers where relevant).
  - Label source-available or non-commercial licenses explicitly; do not describe them as `open-source`.
  - Repositories submitted as open source must include a clear OSI-approved `LICENSE` file (public repositories without a license are all rights reserved by default).
- **Network behavior and telemetry:**
  - Disclose all non-local network behavior accurately: cloud sync, cloud AI models, accounts, telemetry/analytics (especially if enabled by default), online license checks, automatic update checks, and one-time model downloads.
  - Do not claim "no network", "no telemetry", or "no account" if any of the above occur.
- **Availability and link health:**
  - Entries whose project links become unavailable (e.g., 404 repositories) or no longer meet the criteria may be removed.

## Formatting guidelines

- Keep entries in **alphabetical order** within each section.
- Use clean, **canonical URLs** without referral or tracking parameters (no `?ref=`, `utm_*`, etc.).
- Match the existing entry format:
  ```markdown
  - [Project Name](https://canonical-url.example) - Concise, factual description of what it does, how it stores and syncs data locally, its license/commercial status if non-OSI, and any network or telemetry behavior.
  ```
- Keep descriptions concise and factual (typically 1–2 sentences, avoiding marketing superlatives).
- Submit **one project per pull request** unless reorganizing or maintaining the list.

## Pull request requirements

In your pull request description:

1. Link directly to documentation, source code, or a privacy policy verifying:
   - Offline reopening of saved work;
   - Independent backup, export, or user-controlled files;
   - Multi-device sync/collaboration support **or** sync-oriented data structures (e.g., CRDTs, HLCs, append-only logs);
   - License and network/telemetry behavior.
2. Disclose any affiliation (for example, if you are the author or maintainer).
