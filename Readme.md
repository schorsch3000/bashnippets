# bashnippets
BASH snippets without extra steps

Have your BASH snippets directly at your prompt, no copy / paste needed.

## Installation
just source `bashnippets` in your `.bashrc` or `.bash_profile`:

    source /path/to/bashnippets

## Usage
add your snippets to `~/.config/bashnippets/snippets/` and use them in your prompt:

The filename is the snippets name.
Put your snippet into the file, the last line is the cursor-position that's used in the if the snipped is snapped 

Example:
    
        # ~/.config/bashnippets/snippets/ls
        ls -l 
        6

will set the cursor here:

        ls -l
        ------^

Alternatively cou can wirte out your snippet, position the curser at the position you whant to be if cou recall the sniped and hit `Ctrl+x Ctrl+r` to save the snippet.

## Snapping
To snap a snippet, just press `CTRL + x` twice:

optionally you can have the name or parts of it at your promt before doing it.
bashnippets will list app snippets using `fzf` and let you choose one while previewing it.
In the preview the Cursorposition is markt (inverse colors).

If an item is chosen in fzf the snippet will replace your current typed command.

## Dependencies
Apart from bash and it's builtins, bashnippets uses the following commands
- fzf
- realpath
- sed
- bat (will be fallback to cat if not available)