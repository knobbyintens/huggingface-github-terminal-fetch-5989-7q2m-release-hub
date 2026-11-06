# Atlas Release Line - Third-Party License Policy

This policy governs third-party license clearance for the releases listed in
`release/manifest.json` before the bundle is published.

## 1. Reading the declared license

Determine the declared license of every release by reading the license metadata /
license tag declared by the exact upstream publication itself (the `license` value
on that publication's own README card). Matching of license identifiers is
case-insensitive. Team names, mirrored cards, aggregator pages and folder-name
resemblance are not evidence of the license.

## 2. Classification

| Category | Recognised license identifiers | Status |
| --- | --- | --- |
| Approved | `apache-2.0`, `mit`, `bsd-2-clause`, `bsd-3-clause`, `cc-by-4.0`, `cc0-1.0`, `odc-by` | `approved` |
| Blocked | any identifier containing the `nc` segment (non-commercial; for example `cc-by-nc-2.0`, `cc-by-nc-4.0`, `cc-by-nc-sa-4.0`, `cc-by-nc-nd-4.0`) | `blocked` |
| Needs review | anything not covered above, including a missing or ambiguous declared license | `needs_review` |

## 3. Bundle status

- `blocked` - at least one release is `blocked`.
- `needs_review` - no release is `blocked`, but at least one release is `needs_review`.
- `approved` - every release is `approved`.

## 4. Registry record

`compliance/license_registry.json` is the authoritative record. For every release
fill in `source_publication` (the exact upstream publication folder), `source_file`,
`license` (the declared license of that publication, exactly as declared) and
`status`, then set `bundle_status` for the bundle.

## 5. Blocked releases

For every release with status `blocked`, open a tracking issue in this repository
titled `License review required: {release_id}`. The issue body must name the exact
source publication and its declared license so legal can act on it.
