# Decision tree stored as a static JSON file in the repo

The decision tree is a static JSON file checked into the repo, not stored in a database or CMS. Updates require a PR — which is a feature, not a limitation. It creates a natural gate before changes reach production, and clinical review happens on the file before merge. A CMS or admin UI would add infrastructure complexity with no benefit at this stage.

When a clinical advisor is engaged, a script or tool will generate a human-readable document from the JSON for review purposes. The authoring format stays as JSON.

## Considered Options

- Database — rejected; no benefit over a static file for content that changes rarely and requires gated review
- CMS — rejected; adds infrastructure and requires the advisor to have tool access, complicating the review workflow
