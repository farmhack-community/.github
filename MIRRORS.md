# Mirrored Repositories

This file is the authoritative index of every repository mirrored from a Farm
Hack Box Forgejo instance into the `farmhack-community` GitHub organization.

**Source of truth lives upstream on the boxes.** Each row below names the
canonical Forgejo upstream and the date of the last pre-mirror security/PII
audit (see the curation gate in the mirror plan).

| GitHub repo | Forgejo upstream | License | Last audit | Notes |
| --- | --- | --- | --- | --- |
| _(none yet — Phase 2 pending)_ | | | | |

## Mirror mechanism

One-way Forgejo **push-mirror** (Settings → Mirroring → Push Mirror), syncing
on push plus an 8h interval. GitHub never holds canonical history; if this
side ever diverges from upstream, that is a bug — please file an issue.

## Requesting a mirror

Open an issue on `farmhack-community/.github` using the "request a mirror"
template. Some repositories are intentionally never mirrored (box-coupled
config, fixtures referencing real farms, signing keys); those are tracked on
the deferred-audit list in the mirror plan.
