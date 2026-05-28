# Farm Hack Box

Open-source, farm-hosted, federated infrastructure for regenerative
agriculture, food hubs, and the cooperatives that connect them.

## What this GitHub organization is

This is a **read-only mirror** of selected repositories from our source
forges, which run on the Farm Hack Boxes themselves using
[Forgejo](https://forgejo.org/). We mirror to GitHub so that:

- People who don't yet host a box can browse, read, fork, and learn from
  the code, schemas, plans, and docs.
- Search engines and developer-discovery tools — which haven't heard of a
  Forgejo on a farm in Vermont — can find us.
- Reference URLs in papers, talks, certifications, and grant applications
  stay stable.

**The source of truth lives on the boxes, not here.** Every repository in
this org has a canonical upstream on a Farm Hack Box's Forgejo instance.
Commits arrive in this org via one-way push-mirror within minutes of
landing upstream. Issues filed here are read and triaged; pull requests
need a small extra step (see below).

## How to participate

We've designed contribution as a gradient, not a gate. Pick the rung that
matches where you are today:

| You are... | The path is... |
| --- | --- |
| **Curious — want to read** | You're already here. Browse away. Star the repos you want to follow; GitHub will notify you on each mirror sync. |
| **Want to try the workflows for your own project, without committing to hosting a box** | Clone the mirror locally. Each repo's README marks which components decouple cleanly (most schemas, vocabularies, and JSON registries do; bridges and PoS UIs are box-coupled by design). File issues here to ask which pieces are reusable. |
| **Want to file feedback, bug reports, or specifications** | Open an issue here. A maintainer will read, label, and either resolve in-band or port the conversation to the upstream Forgejo for engineering work. |
| **Ready to contribute code, schemas, or plans** | Either (a) host a Farm Hack Box of your own — the box gives you a Forgejo account that federates with the others — or (b) request a federated account from an existing host. Your commits then flow through the federation; mirroring picks them up automatically. |
| **Want to operate a node in the federation** | Same as above, plus join the governance conversation when farmhack.community comes online. |

Hosting a box is how reciprocity works in this network: you get write
access by becoming part of the infrastructure that hosts everyone's
writes. That cost is intentional — it keeps the network resilient and the
contributor base aligned with the people running it.

## Why mirror to GitHub at all, then?

A reasonable question. We do it for discovery, not for dependency. The
boxes run their own forges because:

- Federation needs forges that can talk to each other and to ActivityPub.
- Sovereignty over the substrate matters when the substrate is your farm.
- A network of farmer-hosted forges, each mirrorable to GitHub, gives the
  best of both: open discovery and local control.

If GitHub disappeared tomorrow, it would be an inconvenience for newcomers
finding us — not a crisis for the people running the boxes.

## What is mirrored, what is not

We mirror repositories that are:

- Pure documentation, plans, or specifications
- Schemas, vocabularies, and reference data (commons-registry,
  eta-registry, etc.)
- Public-by-design libraries and templates (claude-harness-seed,
  claude-workflow-archive)
- Public sites

We do **not** mirror:

- Bridge configurations with credentials or signing keys
- Database migration repositories with fixture data that references real
  farms or members
- Anything containing customer, member, or staff personal information
- Per-box operational state, Tailscale addresses, or hostnames

If a repository you'd like to read isn't here, it may be on the
deferred-audit list. Open an issue (template: "request a mirror") and
we'll prioritize. Some repos may never be mirrored — they're either
intrinsically box-specific or contain history that we'd need to rewrite
before publishing, which we'd rather not do.

The current list of mirrored repos, with their upstream Forgejo URLs and
last-audit dates, lives in
[`.github/MIRRORS.md`](https://github.com/farmhack-community/.github/blob/main/MIRRORS.md).

## Issues and pull requests

- **Issues**: welcomed. File them on the relevant repo. A maintainer
  triages weekly. Substantive engineering issues get ported to the
  upstream Forgejo with a back-link.
- **Pull requests**: we can read and discuss them, but to land them we
  need to either (a) replay your commits upstream on Forgejo under your
  federated account, or (b) ask you to re-submit upstream after you get
  an account. We'll guide you through whichever fits. We aren't trying
  to make this awkward — we're trying to make sure the source of truth
  stays on the boxes, where governance and operations sit.
- **Security or takedown issues**: see each repo's `SECURITY.md`. These
  route to the upstream contact directly, not through the mirror.

## Licenses

Each repository carries its own LICENSE; SPDX identifiers are declared
in repo metadata. The org's general posture:

- **Code**: Apache-2.0 by default
- **Documents, plans, schemas**: CC BY-SA 4.0 by default
- **Reference data**: license inherited from upstream source (we cite it)

Per-repo LICENSE files are always the authoritative answer.

## Where to find more

- **Plans and design docs** — see `farm-hack-box-plans` (once published)
  for the strategic context behind what's in these repos.
- **Forgejo, public-facing** — coming online with the farmhack.community
  TLD rollout. Until then, the boxes federate among themselves and a
  public read endpoint is the work-in-progress.
- **Conversations** — community forum URL TBD; for now, GitHub issues are
  the open channel.

## Sovereignty and reciprocity

This network is small, intentional, and aimed at long-horizon resilience
for farms and the cooperatives they belong to. If that resonates,
hosting a box is the most direct way to join. If it doesn't, you're
still welcome to read, learn, fork for your own purposes, and file
feedback. We try to be useful to both kinds of visitor.

---

*This organization is automatically updated from upstream Forgejo
instances. Last sync timestamps are visible on each repo. If you spot
drift — content here that doesn't match upstream — please file an issue
on the affected repo.*
