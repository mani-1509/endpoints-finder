# endpoints-finder

Minimal surface. Maximum visibility.

A zero-dependency JavaScript bookmarklet designed to extract hidden endpoints, API routes, and client-side artifacts directly from live applications.

Built for reconnaissance. Tuned for speed.

---

## Overview

Endpoint Extractor operates entirely within the browser context. It inspects the DOM, crawls loaded scripts, follows source maps, and recursively traces additional assets to uncover exposed infrastructure details.

No installation. No extensions. No noise.

---

## Capabilities

* Enumerates API paths and route patterns
* Extracts absolute URLs and network targets
* Detects WebSocket endpoints
* Identifies GraphQL queries, mutations, and fragments
* Captures fetch, axios, and XHR request targets
* Resolves and parses source maps
* Collects environment variable references
* Discovers public and embedded S3 bucket links

---

## Execution Model

The extractor performs:

* Initial DOM sweep
* Script source enumeration
* Recursive fetch of linked JavaScript files (depth-limited)
* Source map resolution and parsing
* Pattern-based extraction using targeted regex sets

All findings are aggregated in-memory and rendered in a floating inspection panel.

---

## Installation

Create a bookmark and assign the script as its URL.

Execution is triggered manually on any target page.

---

## Usage

1. Navigate to a target application
2. Trigger the bookmarklet
3. Allow background collection to complete
4. Review extracted artifacts in the panel

Each entry is individually copyable. Full dataset export is available via a single action.

---

## Output Structure

* paths
  Relative API routes and endpoint patterns

* fullUrls
  Absolute network targets

* websockets
  WS/WSS connections

* graphql
  Query and mutation signatures

* fetches
  Runtime request endpoints

* sourcemaps
  Source mapping references

* env
  Environment variable keys

* s3
  AWS S3 bucket references

---

## Configuration

Core parameters can be adjusted directly in the script:

* MAX_DEPTH
  Controls recursive crawl depth

* PATTERNS
  Extend or refine extraction logic

* UI Layer
  Modify panel rendering and styling

---

## Operational Context

Intended for:

* Security research
* Application reconnaissance
* Frontend analysis
* Bug bounty workflows

---

## Legal

Use strictly within authorized environments.

The operator assumes full responsibility for compliance with applicable laws and scope boundaries.
