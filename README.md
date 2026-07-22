# Eido releases

This is Eido's **public-but-unadvertised** binary release repository. Public
means that links may be forwarded or discovered; it is not access control.

The initial `0.1.0-alpha.7` candidate is one exact certified pair: macOS arm64
and Windows x64. Both installers must be present for that initial publication.
A correction may publish only the affected platform under a higher version,
with an explicit release record naming the platform, source, and hashes. The
Alpha installers are deliberately unsigned, so the download page explains the
macOS Open Anyway and Windows SmartScreen steps before installation.

Every release records its exact private-source commit, SHA-256 installer
checksums, certification reference, and release notes. To install a corrected
build, return in your browser, download the newer installer, and reinstall it;
your Profile remains separate from the app. The existing updater path remains
in Eido, but this Alpha publishes no updater manifest/checksum assets. Without
those feed inputs the updater remains dormant and cannot discover, download, or
launch a new installer. `SHA256SUMS.txt` is release-integrity evidence, not an
updater input.

Eido does not collect automatic telemetry. Support reports must exclude saved
Ideas, Card text, prompts, assets, API keys, credentials, and private filesystem
paths.

Eido's source repository is private. This repository publishes release policy
and binary artifacts; it does not publish or license the private source code.
