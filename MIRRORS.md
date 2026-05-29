# Mirrored Repositories

This file is the authoritative index of every repository mirrored from a Farm
Hack Box Forgejo instance into the `farmhack-community` GitHub organization.

**Source of truth lives upstream on the boxes.** Each row below names the
canonical Forgejo upstream and the date of the last pre-mirror security/PII
audit (see the curation gate in the mirror plan).

| GitHub repo | Forgejo upstream | License | Last audit | Notes |
| --- | --- | --- | --- | --- |
| [claude-harness-seed](https://github.com/farmhack-community/claude-harness-seed) | `farmhack-boxes/claude-harness-seed` | GPL-3.0 | 2026-05-28 | Reusable Claude Code harness seed. Template addresses sanitized to `${BOX_*}` placeholders upstream before first mirror. |

## Deferred — not mirrored

| Repo | Reason |
| --- | --- |
| `claude-workflow-archive` | Git history contains live credentials (Forgejo OAuth token, farm-pos JWT secret, DB/WiFi passwords) and box-internal addresses across memory/plan archives. Needs full history rewrite + credential rotation before any public mirror. |

## Mirror mechanism

One-way Forgejo **push-mirror** (Settings → Mirroring → Push Mirror), syncing
on push plus an 8h interval. GitHub never holds canonical history; if this
side ever diverges from upstream, that is a bug — please file an issue.

## Requesting a mirror

Open an issue on `farmhack-community/.github` using the "request a mirror"
template. Some repositories are intentionally never mirrored (box-coupled
config, fixtures referencing real farms, signing keys); those are tracked on
the deferred-audit list in the mirror plan.
