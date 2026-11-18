## 0.4.2+ru.3

### Fleet build

The task panel now saves the level it shows: `PATCH /api/tasks/<id>` accepts
`priority` in both shapes (`2` and `"P2"`), refuses anything else with
`E-KANZO-PRIO-001` before the write, and the panel carries the level's badge and
name next to its `select`.

## 0.4.2+ru.2

### Fleet build

Priority field `priority` (0-4 or `P#`), a `prio:` filter, the level on the
card and in the task panel, and the level in both export formats. Schema
version 10; an existing board migrates with every task at `P2`.

## 0.4.2

### Bug fixes

- Fixed `kanzo update` and the board's Update button always failing on Windows (thanks @Bortlesboat). ([#43](https://github.com/emanuele-em/kanzo/pull/43))
- Fixed an agent's Kanzo tools no longer answering after an update, when the agent had cancelled a call before it (thanks @JYunth). ([#45](https://github.com/emanuele-em/kanzo/pull/45))
- Fixed agents that never send `initialize`, like clients on MCP 2026-07-28, staying on the old version after an update (thanks @JYunth). ([#50](https://github.com/emanuele-em/kanzo/pull/50))
- `kanzo export` now stops with a message on a computer that has joined another board, instead of quietly writing its own old board (thanks @Suyog007). ([#49](https://github.com/emanuele-em/kanzo/pull/49))
- Fixed the board and sidebar getting shorter, with blank space below, when something like a browser extension adds an empty element to the page (thanks @qinsx2002). ([#51](https://github.com/emanuele-em/kanzo/pull/51))

### Dependencies

- Updated rmcp to 3.9.0 and toml to 1.2.0. ([#44](https://github.com/emanuele-em/kanzo/pull/44))
