# pstack for AgenC (unofficial adaptation)

This repo is an **unofficial** repackaging of [pstack](https://github.com/cursor/plugins/tree/main/pstack)
by Lauren Tan, from the [cursor/plugins](https://github.com/cursor/plugins) repo, so that the
AgenC CLI (tested with 0.19.9) can install it as a plugin.
It is not affiliated with or endorsed by the pstack author or Cursor.

The skill content is unchanged. Only the plugin packaging differs; see [NOTICE](../NOTICE) for the
exact upstream commit and the full list of changes. The upstream README is kept as is in
[README.md](../README.md).

## Install

From the root of the project you want the skills in:

```sh
git clone https://github.com/jjsgtokbot/pstack-agenc.git /path/to/pstack-agenc
agenc plugin install /path/to/pstack-agenc --scope project
```

AgenC copies the plugin into `.agents/plugins/` in that project.

## Check it

```sh
agenc plugin validate /path/to/pstack-agenc --json   # expect "success": true
agenc skills list --json                            # pstack skills show with "origin": "plugin"
```

With 0.19.9 the install above lists 56 skills with origin `plugin`, one per `skills/*/SKILL.md`.

## License

MIT, same as upstream. The original [LICENSE](../LICENSE) (Copyright (c) 2026 Lauren Tan) is kept verbatim.
