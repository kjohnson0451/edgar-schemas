# edgar-schemas

Shared JSON Schemas for Edgar Pipeline's wire contracts — one source of
truth across the Go/Python split.

## Contents

- `schemas/filing-envelope.schema.json` — `FilingEnvelope`, edgar-fetcher → edgar-parser

## Usage

Consumers fetch a pinned tag at build time (not vendored) and codegen a
native type from it:

```
curl -sL https://raw.githubusercontent.com/kjohnson0451/edgar-schemas/v1.0.0/schemas/filing-envelope.schema.json -o schema.json
```

- Go: `go-jsonschema`
- Python: `datamodel-code-generator`

## Versioning

Plain git tags (`v1.0.0`, ...). Tags pin the whole repo, not individual
files. Bump on any schema change consumers need to pick up.
