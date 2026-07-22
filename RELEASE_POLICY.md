# Release policy

Friends Alpha releases obey these controls:

- Every release starts as a draft. The initial `0.1.0-alpha.7` draft contains
  its exact certified macOS arm64 and Windows x64 installers, checksums,
  private-source commit, certification evidence, and release note before
  publication.
- Friends Alpha installers are unsigned: macOS is ad-hoc signed only and
  Windows has no Authenticode signature. The download page documents the
  operating-system first-open steps without presenting unsigned bytes as
  authenticated publisher output.
- Published releases and their tags are immutable. A version or tag is never
  reused, even after rejection or deletion.
- Candidate and final installers are the same verified bytes. Publication never
  rebuilds or replaces an artifact.
- The paired-platform requirement applies to the initial `0.1.0-alpha.7`
  candidate. A correction may contain only the affected platform, but it must
  use a higher version and an explicit release record naming the platform,
  source, reason, and hashes.
- Drafts and prereleases are ignored by the download page. It links only the
  final release returned by GitHub's `releases/latest` endpoint.
- The release record names the private source SHA and artifact digests. That
  traceability is not a claim that the private build is reproducible or open
  source.
- Updates on both platforms use a manual browser download and reinstall. The
  existing updater path stays in the app but remains dormant because this Alpha
  publishes no updater manifest/checksum assets. It therefore cannot discover,
  download, or launch a new installer. `SHA256SUMS.txt` is release-integrity
  evidence, not an updater input. A correction is a new immutable version,
  never a replacement asset.
- Private source, Profile data, Portable Exports, credentials, source maps,
  tests, fixtures, and internal documentation never belong in this repository
  or its release assets.
