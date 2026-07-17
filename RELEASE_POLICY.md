# Release policy

No product binary has been published yet. Future Eido releases obey these
controls:

- A release starts as a draft. Every required asset, manifest, checksum, SBOM,
  signature result, and release note is attached and verified before one
  publication step.
- Published releases and their tags are immutable. A version or tag is never
  reused, even after rejection or deletion.
- Candidate and final installers are the same verified bytes. Promotion never
  rebuilds an artifact.
- macOS arm64 and Windows x64 are one release set. Either missing or red target
  blocks the whole release.
- Candidate prereleases are ignored by normal clients. Final promotion passes
  through the protected `release-promotion` environment.
- The public manifest records the private source SHA and artifact digests. That
  traceability is not a claim that the private build is reproducible or open
  source.
- Missing signing, notarization, checksum, persistence, canary, or provenance
  evidence fails closed. Users are never coached to bypass operating-system
  security.
