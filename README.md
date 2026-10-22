# GIMP Commons

**An open, community-driven commons for creative assets and editable GIMP projects.**

GIMP Commons is an early-stage project concept for discovering, organizing, sharing, and reusing creative resources around [GIMP](https://www.gimp.org/): brushes, patterns, gradients, palettes, textures, layered project files, and documented workflows.

The goal is not just to build a large asset gallery. It is to preserve the relationship between **assets, editable projects, their sources, licenses, and the methods used to create them**.

> **Status:** Concept / pre-MVP. Product scope and technical architecture are not finalized. This repository currently contains planning documents, not a working application.

## The idea

A GIMP-centered ecosystem that combines:

- **Visual discovery:** previews, search, tags, collections, and creator pages.
- **Reusable assets:** brushes, patterns, gradients, palettes, textures, and other supported resources.
- **Editable projects:** project previews and metadata for XCF files, with links to required assets when available.
- **Provenance:** source, author, license, version, and attribution information that travels with shared resources.
- **Workflow knowledge:** step-by-step methods and notes explaining how an effect or composition was made.
- **Local-first access:** a useful local library and index, with online discovery and sharing where available.

## Guiding principles

1. **Respect creators and licenses.** Never treat an upload as permission to redistribute it.
2. **Keep projects editable.** Prefer source files and structured metadata over flattened previews alone.
3. **Make provenance visible.** Track authorship, origin, license, versions, and dependencies.
4. **Start small.** Build a reliable asset catalog and GIMP hand-off before attempting a large federated platform.
5. **Avoid premature lock-in.** Keep the initial design portable and document technology choices before committing to them.
6. **Design for accessibility and low-resource systems.** Keep discovery and library management usable without requiring a heavyweight stack.

## Initial MVP direction

- Local asset library and searchable metadata index.
- Previews, tags, and collections.
- Import or open supported assets in GIMP.
- XCF project records with preview, metadata, and linked asset references.
- Explicit source and license fields.
- A small catalog of assets that are clearly licensed for redistribution.
- Offline access to the user's local library.

## Documentation

- [Project vision and scope](docs/VISION.md)
- [Initial architecture notes](docs/ARCHITECTURE.md)
- [Roadmap](ROADMAP.md)

## Current non-goals

The first version will not attempt to replace GIMP, recreate every feature of Pinterest, guarantee compatibility with every third-party asset format, or launch a decentralized network before the local library and metadata model are proven useful.

## Contributing

The project is in its planning stage. Early contributions are most useful as focused discussions, use cases, architecture critiques, and small, clearly scoped proposals. See [ROADMAP.md](ROADMAP.md) for the current direction.

## License

No project license has been selected yet. Until a license is added, do not assume that this repository's contents may be redistributed or reused under an open-source license. Individual assets may have separate terms.
