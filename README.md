# Are We Google Cloud Yet?

A collection of Rust packages related to the Google Cloud Platform, in the spirit of [Are We X Yet](https://wiki.mozilla.org/Areweyet).

Stars ⭐ indicate my preferred stack.

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

### yup-oauth2

[![GitHub Repo stars](https://img.shields.io/github/stars/dermesser/yup-oauth2?style=social)](https://github.com/dermesser/yup-oauth2) [![crates.io](https://img.shields.io/crates/v/yup-oauth2.svg)](https://crates.io/crates/yup-oauth2)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/yup-oauth2/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/dermesser/yup-oauth2) ![GitHub contributors](https://img.shields.io/github/contributors/dermesser/yup-oauth2)

## RPC

### googleapis

[![GitHub Repo stars](https://img.shields.io/github/stars/googleapis/googleapis?style=social)](https://github.com/googleapis/googleapis) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/googleapis/googleapis) ![GitHub contributors](https://img.shields.io/github/contributors/googleapis/googleapis)

Not Rust code, but the official API specifications used to support auto-generated REST and gRPC clients.

### googapis ⭐

[![GitHub Repo stars](https://img.shields.io/github/stars/mechiru/googapis?style=social)](https://github.com/mechiru/googapis) [![crates.io](https://img.shields.io/crates/v/googapis.svg)](https://crates.io/crates/googapis)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/googapis/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/mechiru/googapis) ![GitHub contributors](https://img.shields.io/github/contributors/mechiru/googapis)

Auto-generated Rust bindings to gRPC APIs based on tonic. No direct support for authentication; instead, tonic clients can be wrapped in middleware for authentication. Single crate with each API behind a feature flag.

### google-apis-rs

[![GitHub Repo stars](https://img.shields.io/github/stars/Byron/google-apis-rs?style=social)](https://github.com/Byron/google-apis-rs) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/Byron/google-apis-rs) ![GitHub contributors](https://img.shields.io/github/contributors/Byron/google-apis-rs)

Auto-generated Rust bindings to the REST APIs based on hyper. One crate per API; see [list of crates](http://byron.github.io/google-apis-rs/). Uses `yup-oauth2` for authentication.

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

### tracing-stackdriver ⭐

[![GitHub Repo stars](https://img.shields.io/github/stars/NAlexPear/tracing-stackdriver?style=social)](https://github.com/NAlexPear/tracing-stackdriver) [![crates.io](https://img.shields.io/crates/v/tracing-stackdriver.svg)](https://crates.io/crates/tracing-stackdriver)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/tracing-stackdriver/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/NAlexPear/tracing-stackdriver) ![GitHub contributors](https://img.shields.io/github/contributors/NAlexPear/tracing-stackdriver)

A `tracing` subscriber for stackdriver.

### stackdriver-logger

[![GitHub Repo stars](https://img.shields.io/github/stars/kamek-pf/stackdriver-logger?style=social)](https://github.com/kamek-pf/stackdriver-logger) [![crates.io](https://img.shields.io/crates/v/stackdriver_logger.svg)](https://crates.io/crates/stackdriver_logger)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/stackdriver_logger/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/kamek-pf/stackdriver-logger) ![GitHub contributors](https://img.shields.io/github/contributors/kamek-pf/stackdriver-logger)

A `log` subscriber for stackdriver.

### opentelemetry-stackdriver

[![GitHub Repo stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-rust?style=social)](https://github.com/open-telemetry/opentelemetry-rust) [![crates.io](https://img.shields.io/crates/v/opentelemetry-stackdriver.svg)](https://crates.io/crates/opentelemetry-stackdriver)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/opentelemetry-stackdriver/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/open-telemetry/opentelemetry-rust) ![GitHub contributors](https://img.shields.io/github/contributors/open-telemetry/opentelemetry-rust)

[OpenTelemetry](https://opentelemetry.io/) exporter for stackdriver. Writes logs over gRPC.

## Database

### firestore-serde

[![GitHub Repo stars](https://img.shields.io/github/stars/paulgb/firestore-serde?style=social)](https://github.com/paulgb/firestore-serde) [![crates.io](https://img.shields.io/crates/v/firestore-serde.svg)](https://crates.io/crates/firestore-serde)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/firestore-serde/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/paulgb/firestore-serde) ![GitHub contributors](https://img.shields.io/github/contributors/paulgb/firestore-serde)

Conversion between native Rust types and Firestore `Value`s using [Serde](https://serde.rs/). For use with the `googapis` interface to Firestore.

## Compute

### gce-meta

[![GitHub Repo stars](https://img.shields.io/github/stars/mechiru/gcemeta?style=social)](https://github.com/mechiru/gcemeta) [![crates.io](https://img.shields.io/crates/v/gcemeta.svg)](https://crates.io/crates/gcemeta)
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/gcemeta/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/mechiru/gcemeta) ![GitHub contributors](https://img.shields.io/github/contributors/mechiru/gcemeta)

Access to [metadata](https://cloud.google.com/compute/docs/metadata/overview) for VMs running on GCP.

<!--

Template:

[![GitHub Repo stars](https://img.shields.io/github/stars/{REPO}?style=social)](https://github.com/{REPO}) [![crates.io](https://img.shields.io/crates/v/{CRATE}.svg)](https://crates.io/crates/{CRATE})
[![docs.rs](https://img.shields.io/badge/docs-release-brightgreen)](https://docs.rs/{CRATE}/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/y/{REPO}) ![GitHub contributors](https://img.shields.io/github/contributors/{REPO})

-->
