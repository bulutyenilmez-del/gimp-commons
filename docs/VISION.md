# Project Vision and Scope

**Status:** Working draft, 0.1  
**Project:** GIMP Commons

## Problem

Creative assets are scattered across personal folders, forums, asset sites, social feeds, and individual creator pages. Finding something useful is only part of the problem: people also need to know what the asset is, whether it can legally be reused, how it was made, which project used it, and which other files it depends on.

A gallery of thumbnails alone does not solve that problem. A project file without provenance can be difficult to reproduce or safely share.

## Vision

Make creative resources for GIMP easier to discover, understand, reuse, and build upon—while preserving creator attribution, license information, editability, and workflow knowledge.

## Mission

Build an open, community-oriented system for cataloging creative assets and editable projects, starting with a useful local library and adding online sharing only where it improves the experience.

## Intended users

- Digital artists and illustrators.
- Photo editors and compositors.
- Graphic designers.
- GIMP educators and tutorial authors.
- Asset creators who want to share reusable resources.
- People who maintain large local collections of brushes, textures, palettes, and project files.

## Product pillars

### 1. Asset Commons

A searchable catalog of individual resources such as brushes, patterns, gradients, palettes, and textures. Each entry should provide a preview where practical, tags, format details, creator/source attribution, license, version, and import guidance.

### 2. Project Commons

A catalog of editable projects, especially XCF files. Project records should be able to describe previews, metadata, linked assets, dependencies, and the license of the project itself. A preview is useful, but it is not a substitute for the editable source.

### 3. Creator Commons

Creator profiles and collections that make it possible to curate related assets and projects, credit authors, and follow the lineage of derivative work without hiding the original source.

### 4. Workflow knowledge

Reusable production notes: steps, settings, references, and explanations of how a result was produced. Workflows should be connected to the assets and projects they use, rather than existing only as disconnected tutorials.

### 5. GIMP integration

The desktop editor remains the place where editing happens. GIMP Commons should help people find resources and hand them off to GIMP; it should not try to become a replacement editor.

## Differentiator: relationships, not just files

The central product value is a connected graph of:

- creators and sources;
- assets and versions;
- editable projects;
- dependencies and required resources;
- licenses and attribution;
- collections and workflows.

This relationship model should make it easier to answer: “Where did this come from?”, “Can I reuse it?”, “Which assets does this project need?”, and “How was this effect made?”

## Principles

1. **Attribution by design:** origin, creator, and license are first-class metadata.
2. **Editable-first:** preserve source projects when sharing is permitted.
3. **Local-first:** a user's local library should remain useful without a network connection.
4. **Portable metadata:** avoid a design that traps the catalog in one proprietary service.
5. **Incremental complexity:** prove local search and import before federation or social features.
6. **Accessible performance:** favor a responsive interface and modest resource use.
7. **Clear rights boundaries:** metadata about an asset does not imply permission to redistribute the asset.

## Initial non-goals

- Replacing GIMP or duplicating its editing tools.
- Building a general-purpose social network.
- Hosting every asset found online.
- Automatically assuming that public downloads are redistributable.
- Guaranteeing support for every format or every GIMP version in the first release.
- Building peer-to-peer federation before the local data model and core workflow are validated.

## Questions to resolve through prototypes

- Which asset types should the first version import and preview?
- What metadata is essential for assets versus whole projects?
- How should external resources be referenced when redistribution is not allowed?
- What is the smallest useful GIMP hand-off mechanism?
- Which catalog features must work fully offline?
- How should updates, forks, and derivative works be represented?
