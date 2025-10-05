# plgin Registry

Private registry for plgin semantic feature packs.

## Structure

- `index.json` - Main registry index with all published packs
- `packs/` - Individual pack tarballs and metadata

## API Access

This registry is accessed via the Modal proxy at:
- Read: `https://[modal-url]/registry/index`
- Publish: `https://[modal-url]/registry/publish` (authenticated)

## Schema

```json
{
  "version": "1.0.0",
  "updated_at": "ISO-8601 timestamp",
  "entries": [
    {
      "name": "pack-name",
      "version": "1.0.0",
      "description": "Pack description",
      "languages": ["typescript", "javascript"],
      "frameworks": ["react"],
      "author": "username",
      "published_at": "ISO-8601 timestamp",
      "semantic_tags": {
        "architecture": [],
        "patterns": [],
        "ui_ux": [],
        "components": [],
        "dependencies": [],
        "conventions": [],
        "features": []
      },
      "tarball_url": "https://github.com/PR0TO-IDE/plgin-registry/raw/main/packs/pack-name-1.0.0.tgz",
      "checksum": "sha256-hash"
    }
  ]
}
```
