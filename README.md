# Are We Google Cloud Yet?

A collection of Rust packages related to the Google Cloud Platform, in the spirit of [Are We X Yet](https://wiki.mozilla.org/Areweyet).

Stars (⭐) indicate my preferred stack.

## Considerations

- Authentication strategy
- RPC protocol
- Async runtime

## Authentication

### gouth

[![GitHub Repo stars](https://img.shields.io/github/stars/mechiru/gouth?style=social)](https://github.com/mechiru/gouth) [![crates.io](https://img.shields.io/crates/v/gouth.svg)](https://crates.io/crates/gouth)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/gouth/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/mechiru/gouth) ![GitHub contributors](https://img.shields.io/github/contributors/mechiru/gouth)

**Synchronous** auto-renewed tokens.

### google-authz ⭐

[![GitHub Repo stars](https://img.shields.io/github/stars/mechiru/google-authz?style=social)](https://github.com/mechiru/google-authz) [![crates.io](https://img.shields.io/crates/v/google-authz.svg)](https://crates.io/crates/google-authz)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/google-authz/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/mechiru/google-authz) ![GitHub contributors](https://img.shields.io/github/contributors/mechiru/google-authz)

**Asynchronous** auto-renewed tokens. The refreshing token interface is fully async, but the wrapped used for hyper/tonic integration is not; see [my patch](https://github.com/mechiru/google-authz/pull/1) for a fix.

## RPC

### googleapis

[![GitHub Repo stars](https://img.shields.io/github/stars/googleapis/googleapis?style=social)](https://github.com/googleapis/googleapis) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/googleapis/googleapis) ![GitHub contributors](https://img.shields.io/github/contributors/googleapis/googleapis)

Not Rust code, but the official API specifications used to support auto-generated REST and gRPC clients.

### googapis ⭐

[![GitHub Repo stars](https://img.shields.io/github/stars/mechiru/googapis?style=social)](https://github.com/mechiru/googapis) [![crates.io](https://img.shields.io/crates/v/googapis.svg)](https://crates.io/crates/googapis)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/googapis/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/mechiru/googapis) ![GitHub contributors](https://img.shields.io/github/contributors/mechiru/googapis)

Rust bindings to gRPC APIs based on tonic. No direct support for authentication; instead, tonic clients can be wrapped in middleware for authentication. 

### google-cloud

[![GitHub Repo stars](https://img.shields.io/github/stars/google-apis-rs/google-cloud-rs?style=social)](https://github.com/google-apis-rs/google-cloud-rs) [![crates.io](https://img.shields.io/crates/v/google-cloud.svg)](https://crates.io/crates/google-cloud)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/google-cloud/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/google-apis-rs/google-cloud-rs) ![GitHub contributors](https://img.shields.io/github/contributors/google-apis-rs/google-cloud-rs)

Idiomatic Rust bindings for some GCP services, including storage, based on gRPC APIs and tonic. Only supports JSON service account authentication.

## Storage

### cloud-storage

[![GitHub Repo stars](https://img.shields.io/github/stars/ThouCheese/cloud-storage-rs?style=social)](https://github.com/ThouCheese/cloud-storage-rs) [![crates.io](https://img.shields.io/crates/v/cloud-storage.svg)](https://crates.io/crates/cloud-storage)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/cloud-storage/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/ThouCheese/cloud-storage-rs) ![GitHub contributors](https://img.shields.io/github/contributors/ThouCheese/cloud-storage-rs)

Only supports JSON service account authentication (file or directly through non-standard env vars).

### cloud-storage-lite ⭐

[![GitHub Repo stars](https://shields.io/badge/-gitlab-orange)](https://gitlab.com/oasislabs/cloud-storage-lite) [![crates.io](https://img.shields.io/crates/v/cloud-storage-lite.svg)](https://crates.io/crates/cloud-storage-lite)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/cloud-storage-lite/)

Minimal API, for bucket-scoped access; built in service account authentication (standard env var) and pluggable.

## Observability

## Compute

### gce-meta



<!--

Template:

[![GitHub Repo stars](https://img.shields.io/github/stars/{REPO}?style=social)](https://github.com/{REPO}) [![crates.io](https://img.shields.io/crates/v/{CRATE}.svg)](https://crates.io/crates/{CRATE})
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/{CRATE}/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/{REPO}) ![GitHub contributors](https://img.shields.io/github/contributors/{REPO})

-->
