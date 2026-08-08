# Dekglas

**A self-hosted, read-only operations console for infrastructure state you already control.**

Dekglas gives platform and infrastructure teams a shared browser view of their
infrastructure-as-code state without moving that state into another control plane or replacing
their deployment workflows.

> [!IMPORTANT]
> Dekglas is pre-alpha. No supported public image has been released yet, and the current software
> should not be connected to production infrastructure.
>
> Visit [www.dekglas.com](https://www.dekglas.com) again on **August 15, 2026** for the first alpha:
> Pulumi with S3 and S3-compatible DIY backends.

## Links

- [Dekglas website](https://www.dekglas.com)
- [Docker Hub: dekglas/dekglas](https://hub.docker.com/r/dekglas/dekglas)
- [GitHub Container Registry: ghcr.io/dekglas/dekglas](https://github.com/dekglas/dekglas/pkgs/container/dekglas)
  — placeholder; no image is published there yet

This public repository is the distribution and community home for Dekglas. It will contain
supported release information, allowlisted operational documentation, and public feedback. Product
source, internal architecture decisions, internal roadmaps, and private release material are not
published here.

## Why Dekglas

Teams choose self-managed state backends to keep control over where infrastructure metadata lives.
That control can make everyday visibility harder: operators may need direct storage access, local
CLI context, and detailed knowledge of state-file layouts just to answer what exists, what changed,
or whether work is active.

| Outcome | What it means |
| --- | --- |
| Shared inventory | Browse projects, stacks or workspaces, resources, and outputs in one place |
| Faster context | See update history, current locks, health, and relationships without handling raw state |
| Self-hosted control | Keep infrastructure metadata inside the environment and governance model you operate |
| Lower adoption friction | Observe existing state without replacing deployment tools or CI/CD pipelines |
| Reduced change risk | Use read-only backend access and never initiate updates, destroys, imports, or refreshes |

## How it works

Your infrastructure-as-code tool remains the deployment engine and continues writing to the backend
you selected. Dekglas connects separately with read-only access, discovers supported state and
operational metadata, redacts marked secrets, and builds a bounded Dekglas-owned model for its web
console.

Dekglas is designed to:

- run as a self-contained container;
- use read-only backend credentials;
- present projects, stacks or workspaces, resources, outputs, update history, and active locks;
- redact marked secrets without decrypting them;
- collect or transmit no product-usage analytics;
- keep raw state and deployment controls out of the browser; and
- leave existing automation and state layouts unchanged.

Dekglas does not own deployments, edit or offer raw state for download, decrypt protected secrets,
or require a replacement CI/CD pipeline.

## Alpha scope

The August 15 alpha is intentionally narrow:

- Pulumi project-scoped and legacy stack layouts;
- AWS S3 and compatible object-storage APIs;
- a self-hosted, browser-based console;
- SQLite for the local application database; and
- one bootstrap local administrator.

The alpha is for evaluation, not production. Supported image tags, checksums, release notes,
configuration guidance, limitations, and upgrade expectations will be attached to the corresponding
public GitHub release.

## Product direction

Dekglas is intended to grow beyond the initial Pulumi alpha into a self-hosted console for
Terraform, OpenTofu, and Pulumi state stored in backends teams already operate. Planned backend
families include S3 and S3-compatible object storage, Azure storage, Google Cloud storage,
PostgreSQL, and local or shared filesystems.

These integrations are product direction, not a claim of alpha availability. Each will be announced
through a public release when it is ready to evaluate.

## The story behind the name

Dekglas is a stylized form of deck glass, inspired by the deck prisms shipbuilders set into a vessel’s deck to gather daylight and distribute it through the dark spaces below. These small, durable panes improved visibility, safety, and privacy below deck without opening enclosed compartments or relying on fire-lit lamps that could endanger the ship.

Dekglas applies the same principle to infrastructure. State contains a detailed record of what a team operates, but that record often remains hidden inside object storage or another backend. Dekglas brings it safely into view as a shared operational model—without exposing raw state, moving it beyond the environment you control, or introducing another system capable of changing your infrastructure. Observe with read-only access while leaving privacy and deployment controls intact.

## Images and releases

Dekglas will publish one edition-neutral application image. Public image publication will be tied
to a release in this GitHub repository so an image tag can be traced to release notes and
verification material.

| Registry | Image | Status |
| --- | --- | --- |
| Docker Hub | [dekglas/dekglas](https://hub.docker.com/r/dekglas/dekglas) | Public repository; no supported release yet |
| GitHub Container Registry | [ghcr.io/dekglas/dekglas](https://github.com/dekglas/dekglas/pkgs/container/dekglas) | Placeholder; no image published yet |

Do not rely on an unannounced tag. Supported tags and installation instructions will appear in the
matching GitHub release.

## Feedback and security

Public issue templates and support channels will arrive with the alpha.

## Independence and trademarks

Dekglas is an independent product. It is not affiliated with, sponsored by, or endorsed by Pulumi
Corporation; IBM or HashiCorp; The Linux Foundation or the OpenTofu project; Amazon Web Services;
Microsoft; Google; or the PostgreSQL project or PostgreSQL Community Association of Canada. Product
names and trademarks belong to their respective owners.
