# OpenID Connect & OAuth Specification Graph

This repo is a curated dependency graph of the OAuth 2.0, OpenID Connect,
JOSE/JWT, and related identity specifications.
It is documentation only — there is no build, no tests, and no application code.

## Layout

- `graph.md` — the canonical artifact: a single Mermaid `graph LR` diagram of
  every tracked spec and its dependency edges.
- `README.md` — prose overview plus a categorized list of every spec that
  mirrors the nodes in `graph.md`.
- `docs/motivation.md` — why this project exists.
- `docs/recommended-reading-order.md` — a curated learning path
  (intentionally a subset, not an exhaustive list).

## CLAUDE.md / AGENTS.md symlink pattern

`AGENTS.md` is the canonical instructions file.
`CLAUDE.md` is a symlink to it so Claude Code picks it up automatically while
other AGENTS.md-aware tools read the same content — one file to maintain.
Edit `AGENTS.md`; never replace the symlink with a divergent copy.

## Graph conventions

`graph.md` is the source of truth. Each spec appears in **four** places that
must stay in sync:

1. **Node definition** inside the correct `subgraph`
   (`OpenID_Connect`, `OAuth_2_0_RFCs`, `JOSE_JWT`, `Discovery_Metadata`, `UMA`).
2. **Dependency edges** (`A --> B`, meaning "A **normatively** references /
   builds upon B") under the matching `%% ---- Edges ...` comment block.
   Edges track **normative** references only — not informative ones — and aim
   for **completeness**: draw *every* normative reference from A to a spec that
   is already a node, not just the most salient one. Verify against the IETF
   datatracker structured references view
   (`https://datatracker.ietf.org/doc/<rfc-or-draft>/references/`), which
   separates normative from informative, rather than scraping the prose. For
   `openid.net` specs (no datatracker view) use the spec's GitHub source
   markdown, where mmark markers encode reference type: `[@!ref]` is normative,
   `[@ref]` / `[@?ref]` is informative.
3. **Clickable link** in the `click <NodeId> "<url>" "<tooltip>"` section,
   with a tooltip that matches the node label.
4. **README** bullet under the matching `### Specification Categories` heading.

Edges are **normative-only** but otherwise **complete**, which has two
consequences worth stating: the graph is intentionally **not a DAG** — when two
specs reference each other normatively, both edges are drawn, producing cycles —
and the resulting high edge density is a **deliberate goal** (the graph exists
partly to show how interconnected the OAuth/OIDC ecosystem is). Do not prune
edges for readability, and do not "simplify" cycles.

Node id conventions:

- Published RFCs: `RFC<number>` (e.g. `RFC9700`), label
  `"<Title> (RFC <number>)"`.
- Drafts and OpenID/Kantara specs: descriptive PascalCase id
  (e.g. `OAuth2_IdentityChaining`, `OIDC_Core`), label ending in `(Draft)`
  for unfinished work.

URL conventions:

- RFCs → `https://datatracker.ietf.org/doc/html/rfc<number>`.
- IETF drafts → pin to the **latest revision** you verified, e.g.
  `https://datatracker.ietf.org/doc/html/draft-ietf-oauth-...-NN`.
  Prefer the adopted WG (`draft-ietf-...`) document over a superseded
  individual (`draft-<author>-...`) draft.
- OpenID Foundation specs → `https://openid.net/specs/...`.

Node inclusion / removal:

- Do **not** add a node for an IETF draft that was published as an RFC — use the
  RFC node (e.g. `draft-ietf-oauth-discovery` is RFC 8414, not a separate node).
- Remove a node that is superseded or carries no references of its own; a real
  spec that only references out-of-scope specs may stay as an orphan (no edges).

After editing, sanity-check that the node count equals the click-link count
(every node needs exactly one `click`), and that no edge references an
undefined node id — **except** the four intentional ACE edges
(`RFC9200`/`RFC9201` → `RFC7252`, `RFC8152`, `RFC8392`, `RFC8747`), which target
constrained-environment specs (CoAP, COSE, CWT, PoP-for-CWT) deliberately left
out of scope. Treat those four as an allowlisted exception; do not remove them.

## Adding a spec

Use the `add-spec` skill — it walks the four-place update plus reference
verification. The `spec-researcher` subagent fetches a spec's canonical title,
latest revision, and normative references so edges are wired correctly.
Always verify dependency edges against the actual specification text rather
than guessing (see the README Contributing section).

## Markdown conventions

- All Markdown must pass `markdownlint-cli2`; fix issues, don't ask.
  Config lives in `.markdownlint.yaml` (`line_length` 120).
- Follow semantic line breaks in prose: start each sentence on a new line and
  break after major clauses. These breaks affect source/diffs only, never
  rendered output, and never break inside a hyphenated word.
- Do not reflow `graph.md`'s Mermaid block to satisfy prose rules.
