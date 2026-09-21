# Handy Binary RPM

Unofficial Fedora RPM repository for stable [Handy](https://github.com/cjpais/Handy) releases.
The package uses the binaries published by Handy upstream and is available for Fedora 43, 44, and 45 on
`x86_64` and `aarch64`.

## Install

```bash
sudo dnf copr enable countmancy/handy-bin
sudo dnf install handy-bin
```

The package conflicts with an installed `handy` RPM because both packages install the same
application files.

## Updates

The `Update from upstream` GitHub Actions workflow checks the latest non-prerelease Handy
release every six hours. When the version changes, it updates the spec, submits both
architecture builds to [COPR](https://copr.fedorainfracloud.org/coprs/countmancy/handy-bin/),
waits for them to succeed, and commits the version bump.

The workflow requires a repository secret named `COPR_CONFIG` containing the configuration
from the [COPR API page](https://copr.fedorainfracloud.org/api/).
