# Atlas Phase-2 Release Hub

This repository holds the governance records of the frozen Atlas Phase-2 release
bundle together with the upstream publication archive used to audit provenance.

- `release/manifest.json` - frozen releases and their artifact fingerprints.
- `release/cards/` - release cards (card only, no data shards).
- `governance/license_policy.md` - third-party license clearance policy.
- `compliance/license_registry.json` - clearance registry to be completed.
- `upstream/<team>/<publication>/` - upstream publication archive; every publication
  keeps its own README card with the license it declares for itself.

The bundle is not published until every release in the manifest has been classified
and the registry records the outcome.
