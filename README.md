# @tian.zuo/pi-repo-model

Standalone fork of `pi-repo-model`, based on the version currently used in the local Pi setup.

Per-repository default model and thinking-level preferences for the [pi coding agent](https://pi.dev).

## Install

Install this fork directly from GitHub:

```bash
pi install git:github.com/meatRoll/pi-repo-model
```

For a local checkout:

```bash
pi install ./pi-repo-model
```

## How it works

Stores one model preference per repository in `~/.pi/repo-model/config.json`
and applies it at session start (default triggers: fresh start + new session).
An explicit `pi --model ...` takes precedence on startup. Selections are keyed
by git root, so each repository keeps its own preference without touching global
settings or the repo's own `.pi/` folder.

## Commands

- `/repo-model` — pick a model, then a thinking level, from dropdowns.
- `/repo-model provider/model[:thinking]` — set directly, for example:
  `/repo-model cursor/composer-2.5:high`.
- `/repo-model-unset` — clear the current repo's default.
- `/repo-model-list` — list every configured repo.

## Development

```bash
pnpm install
pnpm run check
pnpm test
```

## License

[MIT](LICENSE) © Tian Zuo
