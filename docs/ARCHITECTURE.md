# Initial Architecture Notes

**Status:** Exploratory. No implementation language or framework has been selected.

This document records architectural constraints and a plausible direction, not a final design.

## Proposed shape

### Local library

A desktop-side library stores metadata and indexes files the user chooses to catalog. It should support fast search, tags, collections, previews, and offline use. The index should reference local files rather than silently copying or uploading them.

A small local database (for example, SQLite) is a candidate, not a commitment.

### Asset records

Each asset record should be able to describe:

- stable internal identifier;
- title and short description;
- asset type and file format;
- local location or remote source reference;
- preview location, when available;
- creator and source attribution;
- license identifier or explicit “unknown / not provided” status;
- version and optional checksums;
- tags and collection membership;
- compatible application/version notes where known.

The data model must distinguish “license unknown” from “openly licensed.” Missing information must never be treated as permission.

### Project records

Project records should describe editable source files such as XCF projects and, where possible:

- preview image;
- application and version information;
- canvas dimensions and color-profile notes, when safely available;
- project license and creator attribution;
- referenced assets and dependencies;
- workflow notes;
- source/version relationships.

The first prototype can store user-entered metadata rather than attempting to parse every format automatically.

### GIMP hand-off

The initial integration should be deliberately simple: open a selected file in GIMP, or copy/import a supported asset into a known user-selected location. Exact mechanics depend on platform behavior and GIMP's available interfaces and should be validated with a small prototype.

Do not assume a plugin is required for the first useful release.

### Online catalog and sharing

An online service may later provide public metadata search, creator pages, collections, asset downloads where redistribution is permitted, and versioned records. The local library should remain useful when this service is unavailable.

Federation or peer-to-peer synchronization is a future research area, not an MVP requirement.

## Suggested conceptual entities

- **Asset:** a reusable resource.
- **Project:** an editable composition or document.
- **Creator:** a person or organization credited for work.
- **Source:** the original URL, repository, or other provenance reference.
- **License:** a declared set of reuse terms.
- **Version:** a specific revision of an asset or project.
- **Dependency:** a relationship indicating that a project or workflow uses another resource.
- **Collection:** a curated set of assets and/or projects.
- **Workflow:** documented steps associated with a project or result.

These are conceptual entities. The storage schema should follow prototype findings, not precede them.

## Packaging and metadata

A portable manifest could eventually describe an asset or project package. It should be versioned and document required fields, optional fields, and how unknown values are represented.

Potential fields include:

- manifest schema version;
- item identifier and type;
- title and description;
- files included in the package;
- checksums for integrity checks;
- creator and source;
- license and attribution text;
- application compatibility;
- dependencies and version relationships.

Do not implement a custom package format until real examples show that existing archive formats plus a manifest are insufficient.

## Security and trust

- Treat uploaded files and metadata as untrusted input.
- Never execute scripts, macros, or embedded content automatically.
- Validate archive paths to prevent path traversal during extraction.
- Enforce size limits and fail safely on malformed files.
- Make external links visible before opening them.
- Keep local indexing opt-in and transparent.
- Avoid uploading local paths, filenames, or files without explicit user action.
- Preserve the difference between a preview, a downloadable file, and an editable source.
- Record license/source metadata without presenting it as legal verification.

## Performance constraints

- Search and browsing should remain responsive on modest hardware.
- Generate previews lazily and cache them.
- Avoid scanning the entire filesystem without user consent.
- Support offline access to indexed local content.
- Keep the metadata layer independent from the presentation layer where practical.

## Open decisions

1. Desktop-first application shape and supported platforms.
2. Implementation language and UI toolkit.
3. Local database and schema migration strategy.
4. GIMP hand-off mechanism on Linux, Windows, and macOS.
5. Initial supported asset formats.
6. Online API and authentication requirements, if any.
7. Hosting, storage, moderation, and takedown process.
8. License policy for code, documentation, and contributed assets.
9. Whether any synchronization/federation is necessary after MVP validation.

## Architecture rule

**Do not choose infrastructure before validating the core workflow.** First prove that a user can catalog a local asset, find it again, understand its license/source, and open or use it in GIMP.
