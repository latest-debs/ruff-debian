![ruff for Debian](.github/readme-header.png)

# ruff for Debian

[![Release](https://img.shields.io/github/v/release/latest-debs/ruff-debian)](https://github.com/latest-debs/ruff-debian/releases)
[![Build](https://github.com/latest-debs/ruff-debian/actions/workflows/release.yml/badge.svg)](../../actions)

[ruff](https://github.com/astral-sh/ruff) — an extremely fast Python linter
and code formatter, written in Rust — packaged for Debian as part of
[latest-debs](https://github.com/latest-debs).

Want your own project packaged and maintained this way? See the
[latest-debs packaging service](https://github.com/latest-debs/apt-repo/blob/main/SERVICE.md).

## Install

Via the latest-debs apt repository:

```sh
sudo apt install extrepo  # if not already installed
sudo extrepo enable latest-debs
sudo apt update
sudo apt install ruff
```

Or download a `.deb` from the [Releases](https://github.com/latest-debs/ruff-debian/releases) page:

```sh
sudo apt install ./ruff_*.deb
```

## Verify

```sh
apt-cache policy ruff
ruff --version
```

## Supported distributions & architectures

- Debian Bookworm (12), Trixie (13), Forky (14/testing), Sid (unstable)
- amd64, arm64, armhf, i386 (bookworm/trixie), ppc64el, riscv64, s390x

## Building

Run the [Build ruff for Debian](../../actions) workflow on GitHub with the
desired upstream version. Packaging is driven by
[debian-multiarch-builder](https://github.com/ranjithrajv/debian-multiarch-builder).

## Collaborate with us

latest-debs is a community effort. If you rely on this package and want to
help keep it fresh, watching for a new upstream release or fixing a build
hiccup, we'd love your help. Open an issue on this repo, or email
**latest-debs@users.noreply.github.com** to get involved.

## Disclaimer

Unofficial, volunteer-run packaging — **best-effort, no SLA**.

- **Update cadence:** publishing a release normally triggers an immediate
  apt-repo rebuild via webhook; the ~6h scheduled run is the fallback. GitHub
  outages, a missing trigger token, rate limits, or upstream archive changes
  can delay or skip an update; there is no freshness guarantee.
- **Draft releases:** every build is published as a *draft* that a maintainer
  reviews before promoting, so a new version can lag its build.

For issues with ruff itself, see
[astral-sh/ruff](https://github.com/astral-sh/ruff).

## License

Packaging scripts in this repo are MIT-licensed. The packaged binaries
remain under their upstream license (`MIT` — see
[astral-sh/ruff](https://github.com/astral-sh/ruff)).
