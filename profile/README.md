<p align="center"><img src="https://raw.githubusercontent.com/go-ruby-fast-gettext-locale/brand/main/social/go-ruby-fast-gettext-locale.png" alt="go-ruby-fast-gettext-locale" width="640"></p>

<h1 align="center">go-ruby-fast-gettext-locale</h1>
<p align="center"><strong>Pure-Go fast_gettext locale handling — tag parsing and Accept-Language negotiation (CGO=0).</strong></p>

<p align="center">
  🌐 <a href="https://go-ruby-fast-gettext-locale.github.io">Website</a> ·
  📚 <a href="https://go-ruby-fast-gettext-locale.github.io/docs/">Documentation</a>
</p>

<p align="center">
  <a href="https://go-ruby-fast-gettext-locale.github.io/docs/"><img alt="Docs" src="https://img.shields.io/badge/docs-mkdocs--material-DC2626?style=flat-square"></a>
  <a href="https://github.com/go-ruby-fast-gettext-locale/fast-gettext-locale/blob/main/LICENSE"><img alt="License: BSD-3-Clause" src="https://img.shields.io/badge/license-BSD--3--Clause-blue?style=flat-square"></a>
  <img alt="Go 1.26.4+" src="https://img.shields.io/badge/go-1.26.4%2B-00ADD8?style=flat-square&logo=go&logoColor=white">
  <img alt="Coverage 100%" src="https://img.shields.io/badge/coverage-100%25-1a7f37?style=flat-square">
</p>

---

Pure-Go fast_gettext locale handling — tag parsing and Accept-Language negotiation (CGO=0). It is a pure-Go (no cgo) reimplementation of Ruby's `fast-gettext-locale`, mirroring its
observable behaviour **without any Ruby runtime**. It is a **standalone,
reusable** module — the backend bound into
[go-embedded-ruby](https://github.com/go-embedded-ruby/ruby) by `rbgo`, the same
pattern as go-ruby-yaml — differential-tested against reference Ruby, 100%
coverage, CI green across 6 arches and 3 OSes.

## Repositories

| Repo | What it is |
|------|------------|
| [**fast-gettext-locale**](https://github.com/go-ruby-fast-gettext-locale/fast-gettext-locale) | the library: Ruby's `fast-gettext-locale` in pure Go |
| [**docs**](https://github.com/go-ruby-fast-gettext-locale/docs) | MkDocs Material documentation, versioned with [mike], served at [/docs/](https://go-ruby-fast-gettext-locale.github.io/docs/) |
| [**go-ruby-fast-gettext-locale.github.io**](https://github.com/go-ruby-fast-gettext-locale/go-ruby-fast-gettext-locale.github.io) | the Hugo landing page |
| [**brand**](https://github.com/go-ruby-fast-gettext-locale/brand) | logos and brand assets |

## Principles

- **Pure Go, zero cgo.** Cross-compiles and embeds anywhere; a static binary by default.
- **Reference-faithful.** Output matches reference Ruby (MRI), validated by a differential oracle.
- **Standalone & reusable.** No dependency on the Ruby runtime — the dependency runs the other way.
- **100% test coverage** is the target, enforced as a CI gate.

## Status

**Pure-Go, CGO=0, differential-tested.** A faithful port of Ruby's `fast-gettext-locale`, validated
against the system `ruby` at 100% coverage, `gofmt` + `go vet` clean, CI green
across the six 64-bit Go targets (amd64, arm64, riscv64, loong64, ppc64le,
s390x — including the big-endian lane). It is bound into the
[go-embedded-ruby](https://github.com/go-embedded-ruby/ruby) (`rbgo`) ecosystem
as a native module.

BSD-3-Clause.

[mike]: https://github.com/jimporter/mike
