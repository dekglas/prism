# Prism

**The public distribution and release record for Prism by Dekglas.**

> [!IMPORTANT]
> No supported public release or image is currently published. Do not treat an unannounced
> registry tag, branch artifact, or repository file as a supported release.

## Release records

When a supported release is available, its GitHub Release will identify:

- the immutable image digest and supported version tags;
- release notes, limitations, and compatibility information;
- signatures, provenance, checksums, and software bills of materials; and
- allowlisted installation, configuration, upgrade, recovery, and security documentation.

Supported installation instructions will always point back to the matching release record. There
is no supported `latest`, branch, commit, candidate, or test tag.

## Distribution coordinates

| Purpose         | Coordinate                | Current state                          |
| --------------- | ------------------------- | -------------------------------------- |
| Canonical image | `ghcr.io/dekglas/prism`   | No package or supported tag published |
| Public mirror   | `docker.io/dekglas/prism` | Public repository; no tag published   |

The private candidate registry is not a public installation source. A public version is promoted
from a reviewed candidate by digest, without rebuilding, only after its release record is approved.

## Repository boundary

This repository contains reviewed release records and allowlisted operational documentation.
Product source, internal architecture decisions, roadmaps, private candidate evidence, credentials,
and unannounced product direction are not published here.

The public website is [www.dekglas.com](https://www.dekglas.com).

Until a supported release provides a private reporting process, do not put sensitive vulnerability
details in a public issue.

## Independence and trademarks

Prism is an independent product by Dekglas. It is not affiliated with, sponsored by, or endorsed by
Pulumi Corporation; IBM or HashiCorp; The Linux Foundation or the OpenTofu project; Amazon Web
Services; Microsoft; Google; or the PostgreSQL project or PostgreSQL Community Association of
Canada. Product names and trademarks belong to their respective owners.
