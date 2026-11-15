# Plain

A very lightweight native Mac app to read and edit Markdown. Free. By [Clément Rog](https://clementrog.com).

**[Download Plain](https://github.com/clementrog/plain/releases/latest/download/Plain.zip)** for macOS 26 on Apple Silicon. Signed and notarized. Unzip it and drag it to Applications.

![Plain showing its Welcome tab](plain.png)

## What it does

- Shows Markdown without its markers. The file stays exactly what you typed, byte for byte.
- Saves only when you press ⌘S.
- One window, one tab per file. ⌘← and ⌘→ switch tabs.
- Draws tables. Type `/table` then Return to make one.
- Opens YAML too.
- Never uses the network.

No settings, no themes, no autosave. On purpose.

## With agents

- **See what the agent changed.** When an agent rewrites a file, Plain shows what changed since you last read it: new words in green, a small red mark where text was removed (click it to put the text back). ⌥⌘G goes to the next change, ⌥⌘Y marks them as seen. What you last read stays on your Mac.
- **Keep your unsaved edits.** When the agent changed other words than yours, its changes merge into your text. When you both changed the same words, Plain leaves your text alone and asks when you save.
- **Leave notes for the agent.** Select a passage, ⌥⌘M, type. The note goes in the file as `<!-- note: … -->`. Then tell your agent "do my notes".
- **Let the agent see what you changed** since its last write:

  ```
  /Applications/Plain.app/Contents/MacOS/Plain --changes plan.md
  ```

- **Files that move stay open.** A file an agent renames or moves keeps its tab.
- **Links like `plan.md:42`** open at that line. ⇧⌘O jumps to a heading.
- **Use Plain as your editor** for git commit messages, and for Ctrl-G in Claude Code and Codex:

  ```
  export EDITOR="/Applications/Plain.app/Contents/MacOS/Plain --wait"
  ```

An agent can file a bug for you:

```
/Applications/Plain.app/Contents/MacOS/Plain --feedback
```

## Make it your Markdown app

In Finder, select a `.md` file, File > Get Info, pick Plain under "Open with", then "Change All…".

## Problems

[Open an issue](https://github.com/clementrog/plain/issues/new), or use Help > Send Feedback… in Plain. Issues are public, so leave out anything private.

Plain is free to use. The source is not public.
