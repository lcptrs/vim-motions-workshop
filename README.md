# Vim **Motions** - Why, What, How?

## Outline

## 1. Why even bother with this >50 year old thing (Vi)?

- Allows you to jump editors / IDEs as you can cover most of keybindings with a Vim emulator
- Can get you more efficient: less motion across the keyboard and to the mouse = less strain on your hands and shoulders
- **It's fun!**

## 2. Don't be scared - use VSCode / AndroidStudio (any Jetbrains IDE) / XCode!
VIM Emulators: It's about the motions, not Vim!
- VSCode: Vim
- JetBrains: IdeaVim
- XCode (built-in!): Editor → Vim Mode

## 3. All you *need* to know
`i` or `a`: [i]nsert or [a]ppend here: use your editor as you already know it

## 4. The "weird" part: modal editing
- `esc` or `ctrl-c` for normal (default) mode
    - why is this default?
- navigating the code, doing small edits like deleting, moving, copy (yank) code
- `v` [v]isual mode
    - [v]isually selecting code and do stuff on this

## 5. The fun part: Vim Motions
*hint*: 
- All motions are meant for the normal mode and are **case-sensitive** and the exact keystrokes!

### 5.1 Movements 
   - `h` `j` `k` `l`: should be used instead arrow keys ← ↓ ↑ →
   - `w`: move to beginning of next [w]ord
   - `W`: move to beginning of next [W]ord ignoring punctuation \
   `this.callSomeMethod("something")` is considered a Word and `this.somethingElse("Hello", "Mom")` is considered two words due to the space
   - `f` `F`: [f]ind next (or previous with `F`) occurence of something e.g. `fe` jumps to next `e` character
   - `t` `T`: same as `f` but un[t]il the next occurence, e.g. cursor will be before the searched character instead of on it
   - `*`: find next occurence of word

### 5.2 Editing
  - `x` `X`: delete under cursor (~Del key) or delete before cursor (~Backspace key)
  - `d`: [d]elete under movement (e.g. `dw` to delete word)
  - `D`: [D]elete until end of line
  - `c` `C`: same as `d` but to [c]hange instead, e.g. go into insert mode after delete

### 5.3 Creating a command
  - Motions can be combined to create a command, e.g. with:
  - `Editing[Multiplier]Movement`
  - `[Multiplier](Editing|Movement)`
  - Common examples:
    - `10k` jump 10 lines up
    - `ci(` [c]hange [i]nside [(]brackets
    - `dt(` [d]elete un[t]il next [(]bracket
    - `d3w` [d]elete [3] next [w]ords
    - `3dj` `3dd`  delete next 3 lines including current / delete 3 lines
