[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/MYsTRONOUT/site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/MYsTRONOUT/site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

# site-generator-speed

A faster drop-in for makefun-site 1.0.0. `run(input)` returns exactly the answer
makefun-site's `build` returns for every input — the output tree as a JSON
object of every path it writes and that file's text, byte for byte — but faster:
a single-pass Markdown renderer with run-based escaping, a character-driven
lexer, cached slugs, and front matter parsed without splitting the whole body.

## How to run

```sh
node main.ts
```

It reads every case from `/input/cases.json` (a JSON array of `{id, input}`),
answers each one alone with `run` from `solve.js`, and writes
`/output/answers.json`. Outside a container, `MAKEFUN_INPUT_DIR` and
`MAKEFUN_OUTPUT_DIR` stand in for `/input` and `/output`.

## Files

- `solve.js` — the fast implementation (dependency-free ES module).
- `main.ts` — the driver the harness runs (Node 22, standard library only).

## Bounty

https://make.fun/bounty/site-generator-speed-01-run-20261122
