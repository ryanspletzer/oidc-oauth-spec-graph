---
name: add-spec
description: >-
  Add a new specification (RFC, IETF draft, or OpenID/Kantara spec) to the
  OAuth/OIDC dependency graph. Use whenever the user wants to add or update a
  spec in graph.md — handles the four-place sync (node, edges, click link,
  README) and verifies references against the source document.
---

# Add a spec to the graph

`graph.md` is the source of truth; `README.md` mirrors it. A spec lives in
**four** places that must stay in sync. Do all four for every spec.

## 1. Research the spec (do not guess)

Delegate to the `spec-researcher` subagent (or fetch the datatracker/openid.net
page yourself) to obtain:

- canonical **title**,
- latest **revision** number (for drafts),
- canonical **URL** (prefer adopted `draft-ietf-...` over individual drafts),
- the **normative references** to specs already in the graph.

Edges must reflect what the document actually references — confirm against the
spec text, not memory. Use the IETF datatracker **structured references view**
(`.../doc/<doc>/references/`, which separates normative from informative) for
RFCs and drafts; for `openid.net` specs use the GitHub source markdown
(`[@!ref]` normative, `[@ref]`/`[@?ref]` informative). Draw **all** normative
references to in-graph specs (completeness); normative only.

## 2. Pick id, label, and subgraph

- RFCs: id `RFC<number>`, label `"<Title> (RFC <number>)"`.
- Drafts / OpenID / Kantara: descriptive PascalCase id
  (e.g. `OAuth2_IdentityChaining`); label ends in `(Draft)` if unfinished.
- Place the node in the right `subgraph`: `OpenID_Connect`, `OAuth_2_0_RFCs`,
  `JOSE_JWT`, `Discovery_Metadata`, or `UMA`.

If the spec already exists, this may be an **update** (e.g. bump a draft to a
newer revision, or repoint a superseded individual draft to the WG version) —
edit in place instead of adding a duplicate node.

## 3. Edit `graph.md` (three sections)

1. **Node** — add the `Id["Label"]` line inside the chosen subgraph.
2. **Edges** — add `Id --> Dep` lines under the matching `%% ---- Edges`
   block, one per normative dependency that exists in the graph.
3. **Click link** — add `click Id "<url>" "<tooltip>"`; tooltip matches the
   label.

## 4. Edit `README.md`

Add a bullet under the matching `### ...` category heading describing the spec
in one sentence, consistent with the existing entries.

## 5. Verify

- Node count must equal click-link count:
  `grep -cE '^\s+[A-Za-z0-9_]+\["' graph.md` vs `grep -cE '^\s+click ' graph.md`.
- No edge may reference an undefined node id, except the four allowlisted ACE
  externals (`RFC7252`, `RFC8152`, `RFC8392`, `RFC8747`).
- Run the markdown linter (`mdlinter` skill or `markdownlint-cli2`) and fix.
