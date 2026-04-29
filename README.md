# pi-config

My personal [pi](https://pi.dev/) configuration.

## About me

I like:

- simplicity and minimalism
- working in the terminal
- coding
- markdown (e.g., README and TODO files and docs in a git repo)
- documentation (ok, maybe not like :P, but I write it anyway because I'm forgetful)
- editing in neovim (coming from emacs evil-mode)

I care about:

- agent permissions
- concise, short, no-fluff answers from the agents
- guidelines per programming language
- clean code
- documenting design decisions for later reference (I should do more)
- staying up-to-date with the latest tools and techniques

I don't:

- trust agents yet, but I'm also lazy to check every command they execute
- use subagents a lot

## Features

- **AGENTS.md** — global agent instructions: who I am, rules, blacklist, TDD, KISS
- **settings.json** — theme, packages, and [`pi-guard`](https://github.com/jdiamond/pi-guard) rules: auto-allows safe commands (`find`, `ls`, `grep`, `git status/diff`, `uv run pytest`); blocks dangerous ones (`rm`, `git merge/reset/rebase/revert`, `uv tool`) and blacklisted files (`*.env*`, `*secret*`, `*password*`, `*token*`, `secrets/**`, `credentials/**`, `*.pem/key/crt/p12`); asks for everything else

## Deploy

Clone directly as `~/.pi/agent/` — pi auto-discovers everything from there:

```bash
git clone git@github.com:dratasich/pi-config.git ~/.pi/agent

# install extensions
pi install npm:pi-guard
```

To update:

```bash
cd ~/.pi/agent && git pull
```

## References

- My personal [opencode-config](https://github.com/dratasich/opencode-config)
- Input from HazAT's [pi-config](https://github.com/HazAT/pi-config)
