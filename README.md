# Clean Commits
A convention for cleaner, more expressive commit messages.

## Foreword
Just use [standard commit messages](https://cbea.ms/git-commit/) until the project gets big enough that a more involved convention adds value.

## Format
```
+sys.subsys: Provide terse summary of commit

Sometimes, additional description or details can be helpful. Such details
can be provided here.

Refs: #123
```

| Component      | Description                                      |
|:---------------|:-------------------------------------------------|
| `+`            | The type of commit (see below).                  |
| `sys.subsys`   | Context for the commit, in common dot notation.  |
| `Provide...`   | Good ol' imperative summary of commit.           |
| `Sometimes...` | Additional details/description (optional).       |
| `Refs:`        | Callout for PRs/issue numbers (when applicable). |


## Contexts
- Write in dot notation: `sys.subsys`
- Concatenate with pipe (`|`) : `sys1|sys2`
    * Or split into two separate commits (usually preferable).
- If commit affects more than ≈2 subsystems, use keyword `all` for the context.


## Types

| Type     | Symbol | Mnemonic                                                                             |
|:---------|:------:|:-------------------------------------------------------------------------------------|
| Fix      | ~      | A change (fix). Includes bugfixes.                                                   |
| Feat     | +      | Something new and shiny. Shiny new "features".                                       |
| Chore    | -      | Something boring, repetitive, and easy to ignore. But necessary.                     |
| Style    | *      | A purely cosmetic fix. Like when correcting spelling/grammar in texts/chats.         |
| Refac    | =      | Things ultimately work the same (equally) before and after.                          |
| Perf     | $      | Money. (Run)time is money.                                                           |
| Tests    | %      | Being within some quantifiable metric of some explicit target.                       |
| Revert   | @      | "At". Go back to some previous place/location.                                       |
| Build/CI | #      | "Press the pound key" to build/distribute the software.                              |
| Blank    | _      | Blank. Unsure of type. It may become clear naturally, after a few more commits.      |
| Docs     | ?      | But who/what/where/when/why/how? ___Never used alone - use to prefix other types.___ |
| Break    | !      | Be careful! ___Never used alone - use to prefix other types.___                      |

Unassigned: `&^/\|,;"'()[]<>`


## A Word on Usage
Just use [standard commit messages](https://cbea.ms/git-commit/) until the project gets big enough that a more involved convention adds value.


## Examples
## Sel
- `~nvim.plug: Update several plugin configs to maintain compatibility`
- `+all: Stop tracking several unnecessary files`
- `-nvim.keys: Do commits in new tab`
- `*nvim.keys: Whitespace`
- `=nvim.opts: Clear command line more cleanly`
- `$nvim.snip: Exit snippets more cleanly`
- `?nvim.keys: Explicitly bind jump actions`
- `%all: Tweak usernames/emails`
- `@htop: Add config`
- `#all: Finish adding files after PII scrub`
- `!+nvim.keys: Add git rebase binding`
- `~mouse|keys: Update bindings per nvim changes`

## Dokugaku
- `+dsa.cdp: Finish lesson 7`
- `+dsa.clrs: Read chapter 5`
- `+py.aoop: Complete lesson 5`
- `+py.ohd: Complete day 6`
- `+rs.lings: Finish tutorial 5`
- `+rs.book: Read chapter 3`
- `+rs.byx: Finish part 3`
- `+vim.pv: Finish next part`
- `+db.mongo: Finish part 3`
- `-watch: Update Rust watchlist`

