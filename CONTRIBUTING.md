# Contributing

Thanks for helping grow this curated list of Claude Opus 5.5 use cases.

## What belongs here

We welcome **use cases** — playable games, interactive 3D scenes, films/animations, agent/engineering showcases, and related curated collections — that were built with or prominently feature **Claude Opus 5.5**.

We generally **do not** list pure prompt-leak / system-prompt dumps in the main sections. Benchmarks and analysis posts are welcome under their own section.

## How to add an entry

Open a pull request that updates both:

1. `README.md` — add a bullet under the right section
2. `data/usecases.json` — append a matching object (keeps the list machine-readable)

### Required fields

| Field | Description |
| --- | --- |
| **title** | Short, descriptive name of the use case |
| **url** | Primary link (GitHub repo, article, or landing page) |
| **description** | One sentence: what it is and why it is interesting |
| **source** | One of: `github`, `x`, `hn`, `web`, `official` |

### Optional fields

| Field | Description |
| --- | --- |
| **demo_url** | Live / playable URL when one exists |
| **stars** | GitHub star count at time of addition (integer, or omit) |
| **notes** | Extra context (HN thread, X handle, A/B pairing, etc.) |
| **category** | One of: `official`, `games-3d`, `creative`, `agent`, `collections`, `benchmarks`, `showcase`, `videos` |
| **author** | Creator handle (e.g. `@handle`). Required for `videos` entries sourced from X |
| **video_type** | For `videos` entries: `motion-design`, `explainer`, `short-film-music`, `game`, `3d-shader`, `ad-launch`, or `comparison-pipeline` |

### `data/usecases.json` shape

```json
{
  "id": "kebab-case-slug",
  "title": "Demo Title",
  "url": "https://github.com/org/repo",
  "demo_url": "https://example.com/live",
  "source": "github",
  "category": "games-3d",
  "stars": 42,
  "notes": "Optional context",
  "added": "2026-09-24"
}
```

Use `null` for `demo_url` or `stars` when unknown.

### Video entries from X

The **Videos (from X)** section lists video works made with Opus 5.5. Each entry must link the creator's original post (`https://x.com/<handle>/status/<id>`), whose text makes clear Opus 5.5 was used and which carries a video (or links directly to the video work). Add `"category": "videos"`, `"author": "@handle"` and a `video_type`, credit the author in the README bullet, and list the same video only once (keep the original creator's post, not reposts or quotes).

```md
- [Title](https://x.com/handle/status/123) — @handle — One-sentence description.
```

### README bullet style

```md
- [Title](https://github.com/org/repo) — One-sentence description. [Live demo](https://example.com).
```

Keep descriptions in complete English sentences. A short Chinese subtitle on the project is fine elsewhere; list entries stay English-first.

## PR checklist

- [ ] Link resolves and clearly relates to Opus 5.5
- [ ] Entry is not a duplicate of an existing item
- [ ] `README.md` and `data/usecases.json` stay in sync
- [ ] Live demo URL included when publicly available
- [ ] Source (`github` / `x` / `hn` / …) is accurate

## License

By contributing, you agree your additions are released under [CC0 1.0](LICENSE) (same as the rest of this list).
