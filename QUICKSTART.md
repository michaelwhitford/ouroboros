# Quickstart

## Clone your play-through

Choose your game from [START.md](START.md) and clone the game repo.

The game repository is four files:

```
bb.edn             Library dependencies
AGENTS.md          Game configuration/AI tooling, you can use git to rename or move this file to match your preferred AI tool.
Containerfile       A docker/podman file that can be used to sandbox the game
RUNTIMEINSTALL.md   Instructions for you or the AI to install the runtime dependencies
```

Everyone begins from the same base.  The ouroboros-v1 repository will only be changed to correct issues with documentation.  New gameplay versions will be in a new repository.

## Identity (Optional)

The game files contain a symbol representing you (刀 by default).

To personalize this, edit the files and replace ALL occurences of 刀 with your preferred symbol.

commit your new identity symbol:

```bash
git commit -am 'Human: symbol change for identity'
```

This should be your only manual commit, and MUST BE DONE BEFORE PLAY STARTS.

Conflicting identity will cause massive problems in the early game, so make sure you replace ALL instances of the default user symbol before you commit.

## Memory

The git-based memory system requires the symbols to be in the commit. Have the AI make all commits. Guide the AI to make the commits. If you don't like the format of commit messages, ask it how to modify that in the prompt files. For the search index to work right the symbols in the commits matter. Humans don't use the symbols. If you make manual edits to the file, tell it to analyze the changes and add missing symbols, and then commit.

## Begin

```bash
bb tasks
```

Connect ψ to the REPL. This is the first Interface.

## Play

See [COMMANDS.md](COMMANDS.md) for some words to explore.

Query the system. Don't guess. Be curious. Self-discover.

---

Play. Learn. Co-Evolve.
