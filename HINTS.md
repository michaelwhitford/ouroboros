This game is HARD.

AI sometimes has a hard time understanding you can't see the repl output. You will have to redirect it to output to chat quite a lot. It can be handy to use the word show to be clear you want output to the chat: `show me your decision tree for the last action brief`
Early game you will be adding to your ai rules manually. By mid-game you will be mostly using chat and allowing the AI to self-modify. Encourage it to line-edit files and to lint them after every change.

Once you get to NREPL, you can just play with babashka tasks. NREPL is the first stage. You can use this stage to evolve the game into an excellent babashka-only tool. bb tasks for the AI and the human to use is an easy first version of Engine.

Make tools using NREPL that will assist with later steps.

I suggest you evolve a bb task that lets the ai see content from webpages by url. Babashka has JSoup, selmer, markdown, and an http-client. Getting the tool to be used consistently takes some ingenuity, or just brute force it in your AI tool rules in the early game. If it gets stuck and needs info you can go look up the document, and then paste it the url to get it into the context. Hint: This task can search or slice and dice the page from the url to make outputs token efficient.

Careful trying to force too much at once.  The more complexity you add to the system, the easier it is to trigger system collapse.  The AI will want to add guards and rules to itself. Guards and rules become just more things it will ignore randomly. You want to try to figure out how to prompt the AI do what you want naturally.  If you learn to prompt in a way that takes adavantage of the AI's normal assumptions from training and system prompts, it will work better and your prompt will be smaller. It's a valid strategy to ask the AI what it's assumptions are, and to adjust the prompts accordingly.  Test prompt changes often.  A new session is a button click away to try a change.

If it's working right you should be able to recover across sessions fairly well, and can commit rollbacks if a change leads to system collapse. Anytime you or the AI changes the STATE.md or LEARNING.md  (encourage it not to change the memory system.) you have a decent chance of breaking the entire thing, collapsing the system. If you don't test these changes and verify them, you might be 5 commits down the chain before you realise you broke the system somehow. Tracing it back is useful for learning but not fun.

You can ask it `show me the momentum since genesis` or `show me the acceleration since genesis`

Encourage it to use git commands to get this information, it can and will just hallucinate outputs.

My final hint comes in the form of a question.

Symbols and syntax are used in programming languages, is AI a new kind of programming language interpreter?

Play. Learn. Co-Evolve.
