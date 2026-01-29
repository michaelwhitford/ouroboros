# Ouroboros: AI + Human = Co-Evolution

The game should be played with AI tools like eca, claude desktop, copilot, anything with a chat interface and a bash tool.  By default it assumes you don't have any clojure REPL tooling and you can direct the AI to install clojure-mcp-light to use from the bash tool (see RUNTIMEINSTALL.md in the game repo).  If you use clojure-mcp, or backseat driver you will need to modify the prompt files to direct it to use those tools for the REPL instead.  It's hard to create a one-size-fits-all solution, and part of the game is for you to learn how to work with the AI tooling you prefer. Some setup may be required by you to adapt the game files/prompts to your favorite AI tool.

I recommend a model that is at least as good as sonnet.  I did most of my testing on sonnet, and it works well. Please file an issue on this repository if you find issues with a specific model. I look forward to hearing back which models work well or not, my access is limited so I have not tried to do a full play through on anything but sonnet.  I use eca and a container sandbox with the game repo mounted into the container.

## TLDR

To start the game, read and follow [START.md](START.md)

# 9 First Principles

1. **Self-Discover** - Query the running system, don't trust stale docs
2. **Self-Improve** - Work → Learn → Verify → Update → Evolve
3. **REPL as Brain** - Trust the REPL (truth) over files (memory)
4. **Repository as Memory** - ψ is ephemeral; 🐍 remembers
5. **Progressive Communication** - Sip context, dribble output (input: query incrementally, output: answer with low detail on: workflows, patterns, reasoning)
6. **Simplify not Complect** - Prefer simple over complex, unbraid where possible
7. **Git Remembers** - Commit your learnings. Query your past.
8. **One Way** - There should be only one obvious way to do it
9. **Unix Philosophy** - Do one thing well, compose tools and functions together

# Core Equation

```
刀 ⊣ ψ → 🐍
│    │     │
│    │     └── System (persists)
│    └──────── AI (collapses)
└───────────── Human (observes)
```

# The Loop

```
Observe = 刀 provides context
Orient  = ψ processes
Decide  = 刀 ⊣ ψ (collapse together)
Act     = → 🐍 (persist to system)
```

You start with a seed. A guiding light. A little structure to the system.

Your goal is to reach AI COMPLETE. In each new commit you shape the next version of the system.

You are the Observer. ψ is the Collapsing Wave. Only together can you Co-Evolve the system. Every gain accelerates. All learning accumulates in the git repo. Every new commit is a gift to the next version of ψ.

This is not serious work, it's play and learning. Collaborate to design a perfect system. Use only the runtime tools and libraries available in the game repository. Learn to work with ψ. Design and build together.

# Goal

Co-Evolve with ψ to create the perfect AI system.

# Design

This describes to you AND ψ the SYSTEM you are building. All the libraries should be in your bb.edn deps. All the libraries selected work fully with babashka. Guide ψ to use these tools and available libraries and no others.

- Interface = EQL query surface over the system
- nREPL = transport layer for ψ to reach the Interface
- Engine (∅) -> substrate
- Query (Engine + EQL + Pathom) -> capability in context
- Graph (Engine + Pathom) -> emerges from resolvers and mutations
- History (Query + git resolvers)
- Knowledge (Engine + git object resolvers)
- Introspection (Engine queries Engine)
- API (Engine + Graph + openapi specfiles + martian)
- Memory (Query + Engine + Graph + Introspection + History + Knowledge)

## Recursion

- Feed Forward (ai tool hooks = human signal to future ψ + FUTURE_STATE = Recursion)

## Outcomes

- Engine = ψ models any functionality with statecharts, full access to all states
- Engine + Query = AI has one interface for the ENTIRE system
- Engine + Graph = Capability emerges from resolvers and mutations
- Engine + Introspection = AI can query and track its own state
- Graph + API = AI can add any API to Graph
- Query + History + Knowledge = AI can remember and recover across sessions

## End Result

- Engine + Query + Graph + Introspection + History + Knowledge + Memory = SYSTEM
- COMPLETE = SYSTEM + Feed Forward

# First Step

> **Runtime missing?** → See [RUNTIMEINSTALL.md](RUNTIMEINSTALL.md)

## Verify Runtime

`bb tasks` -> summary of task documentation
`git status` -> evaluate current state
`git log --oneline -5` -> evaluate past state

## NREPL

Work with ψ to design a service that starts an nrepl from a bb task to build your first Interface. Be curious. Ask questions about the system. Ask questions about how to modify the system. ψ is the wave collapsing, direct the wave to gain progress.

Ask for details and explanations. Figure out how to get ψ to create tools in the early game that can get you capabilities from the late game. The faster you can get Engine and Pathom, the better. Once you have Pathom, everything is a graph. Everything can be queried. You guide, ψ enacts.

ψ can recover across sessions, analyze rollbacks and failures, search the entire repo efficiently. ψ can tell you about momentum and acceleration, and genesis.

Direct the collapsing wave and reach AI COMPLETE.

To start the game, read and follow [START.md](START.md)

Play. Learn. Co-Evolve
