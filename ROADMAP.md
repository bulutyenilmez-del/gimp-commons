# Roadmap

**Status:** Draft. Milestones are goals, not delivery promises.

## Phase 0 — Define the problem

- [x] Establish the project repository.
- [x] Write the initial vision and scope.
- [x] Record architecture constraints and open decisions.
- [ ] Collect concrete user workflows and examples.
- [ ] Decide the first supported operating system(s).
- [ ] Agree on a license strategy before accepting code or assets for redistribution.

**Exit criterion:** The first user problem and a narrow MVP are written down clearly enough to prototype.

## Phase 1 — Local catalog prototype

- [ ] Add a local asset record and metadata model.
- [ ] Index a user-selected folder; do not scan the entire filesystem by default.
- [ ] Search by title, type, and tags.
- [ ] Display a preview when one is available.
- [ ] Support collections or saved groups.
- [ ] Record source, creator, license status, and local path.
- [ ] Keep the catalog usable offline.

**Exit criterion:** A user can add an asset, find it again, and understand what is known—and unknown—about its origin and reuse terms.

## Phase 2 — GIMP workflow

- [ ] Validate opening selected files in GIMP across the chosen platform(s).
- [ ] Add a safe hand-off for supported brushes, patterns, palettes, or other selected formats.
- [ ] Document compatibility limits.
- [ ] Test with a small, curated set of clearly licensed sample assets.

**Exit criterion:** Finding an asset reliably leads to using it in GIMP without confusing or risky file operations.

## Phase 3 — Editable project records

- [ ] Add XCF project entries and previews.
- [ ] Record project attribution and license separately from asset licenses.
- [ ] Link projects to known assets and dependencies.
- [ ] Add workflow notes and source/version relationships.

**Exit criterion:** A project record communicates what the project is, where it came from, what it needs, and how it may be reused.

## Phase 4 — Community catalog

- [ ] Define the public metadata/API model.
- [ ] Add creator pages and collections.
- [ ] Publish only files that are permitted to be redistributed; allow metadata-only references where appropriate.
- [ ] Establish moderation, reporting, correction, and takedown processes.
- [ ] Add version history and attribution for derivatives.

**Exit criterion:** People can discover and share resources with transparent provenance and rights information.

## Later research — Federation and synchronization

Consider decentralized distribution, synchronization, and federated catalogs only after the local workflow, metadata model, and community trust requirements are validated.

## Not yet decided

- Implementation language and UI toolkit.
- Database choice.
- Exact package/manifest format.
- Server hosting and storage model.
- License for the application and documentation.
- Asset contribution and moderation policy.

These decisions should be made deliberately and documented as they become necessary.
