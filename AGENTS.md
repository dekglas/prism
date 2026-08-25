# Agent guidance

## Repository purpose

This public repository distributes Prism container-image release information and user
documentation. It is not the product source, design record, implementation repository, or internal
planning workspace.

## Suitable changes

Keep changes public-safe and limited to:

- documentation for installing, configuring, operating, upgrading, and troubleshooting Prism;
- public container coordinates and versioned release information that already exists;
- public security-reporting, support, contribution, conduct, and legal documentation.

Do not add product source code, internal designs, implementation details, private automation,
credentials, customer data, private infrastructure information, internal repository names or
paths, or unreleased plans. Do not infer product behavior from this repository when the public
documentation does not state it.

Treat published versioned release records and documentation snapshots as immutable. Correct an
error in a later published version instead of rewriting an existing record. Keep image names,
versions, and digests consistent with the public release record, and do not invent unpublished
artifacts.

## Security and legal

Never post secrets, customer information, infrastructure data, or vulnerability details in a
public issue. Use the repository's private security-reporting feature for suspected
vulnerabilities.

Do not change licensing terms, redistribution rights, or other legal language without explicit
owner and legal approval.

## Review

Before proposing a change:

- confirm that every statement is appropriate for a public user-facing repository;
- check links, commands, image references, versions, and digests for consistency;
- scan the changed content for secrets and private operational information;
- run `git diff --check`.

This repository contains no product build or implementation test suite.
