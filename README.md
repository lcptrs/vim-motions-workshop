# Vim **Motions** - Why, What, How?

## Outline

1. Why even bother on this >50 year old thing (Vi)?
    - Allows you to jump editors / IDEs as you can cover ~80% of keybindings with a Vim emulator
    - Can get you more efficient: less motion across the keyboard and to the mouse = less strain on your hands and shoulders
    - **It's fun!**
2. Don't be scared - use VSCode / AndroidStudio (any Jetbrains IDE) / XCode!
    - VIM Emulators: It's about the motions, not VIM!
        - VSCode: Vim
        - JetBrains: IdeaVim
        - XCode (built-in!): Editor > Vim Mode
3. All you **need** to know
    - `i` or `a`: [i]nsert or [a]ppend here -> use your editor as you already know it
4. The weird part: modal editing
    - `esc` or `ctrl-c` for normal (default) mode
        - navigating the code, doing small edits like deleting, moving, copy (yank) code
        - why is this default?
    - `v` [v]isual mode
        - [v]isually selecting code and do stuff on this
5. The fun part: Vim Motions \
   *hints*: 
   - All motions are meant for the normal mode and  are **case-sensitive** and are the exact keystrokes!
   - Motions can be combined to create a command, e.g. with:
        - `Editing[Multiplier]Movement`
        - `[Multiplier](Editing|Movement)`

   1. Movements 
       - `h` `j` `k` `l`: should be used instead arrow keys ← ↓ ↑ →
       - `w`: move to beginning of next [w]ord
       - `W`: move to beginning of next [W]ord ignoring punctuation \
       `this.callSomeMethod("something")` is considered a Word and `this.somethingElse("Hello", "Mom")` is considered two words due to the space

   2. Editing
      - `x` `X`: delete under cursor (~Del key) or delete before cursor (~Backspace key)
