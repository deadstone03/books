# practical vim


## the vim way

## modes

### Normal

### Insert

### Visual

### Command Line

## Files

### Manage Multiple Files

### Open Files and Save Them to Disk

## Getting Around Faster

### Navigate Inside Files with Motions

### Navigate Between Files with Jumps

## Registers

### Copy and Paste

#### 59. Delete, Yank, and Put with Vim’s Unnamed Register

- `xp` transposing characters

- `ddp` transposing lines

- `yyp` duplicate lines

#### 60. Grok Vim’s Registers

- Addressing a Register

	- `”{register}` before delete, yank or put

- the unnamed register `”`

- the yank register `0`

- `:reg` see the number register’s value

- named registers `a-z`

- the blackhole register `_`

- the system clipboard `+` register

- the recent selection `*` register

- expression register `=`

- read only registers

	- `%` name of current file

	- `#` name of alternate file

	- `.` last inserted text

	- `:` last Ex command

	- `/` last search pattern

#### 61. Replace a Visual Selection with a Register

- swap two words

#### 62. Paste from a Register

- paste character-wise regions

	- insert mode `<CTRL-R>{register}`

- paste line-wise regions

#### 63. Interact with the System Clipboard

- `:set paste`

- `:set nopaste`

- `:set pastetoggle=<f5>`

- or paste from `+`

### Macros

#### 64. Record and Execute a Macro

- capture a sequence of commands by recording a macro

	- `q` to start and stop

	- `q{register}` store macro in register

	- `:reg a` to show the content

- play back a sequence of commands by executing a macro

	- `@{register}`

	- `@@` most recently

- execute the macro in series

- execute the macro in parallel

#### 65. Normalize, Strike, Abort

- normalize the cursor position

	- `n`

	- `gg`

	- `0`

- strike your target with a repeatable motion

- abort when a motion fails

#### 66. Play Back with a Count

#### 67. Repeat a Change on Contiguous Lines

- serial

	- add `l` at the end

- parallel

	- select then `:normal @a`

#### 68. Append Commands to a Macro

- `qa` to record, `qA` to append to register a

#### 69. Act Upon a Collection of Files

- `:edit!` revert all the changes not written to the file yet

- parallel

	- `:argdo normal @a` do the macro to all files in args

- series

	- add `:next` to the end of the macro

- `:wall` save changes to all files

- `:wnext` write and go to the next file

#### 70. Evaluate an Iterator to Number Items in a List

- `:let i=0` set variable i to 0

- `:echo i` get the value of i

- `:let i += 1`

- `<C-r>=i<CR>` to insert the value of i

#### 71. Edit the Contents of a Macro

- `~` to toggle the case of the letter

- paste the Macro into a Document

	- `:put a` put the a register content in a file
	  what’s the difference between `:put a`, `”ap` and `i<C-r>a`

- edit the file

- yank the macro from the document back into a register

- `:h function-list`

## Patterns

### Matching Patterns and Literals

#### 72. Tune the Case Sensitivity of Search Patterns

- ‘ignorecase’ setting globally

- `\c` ignore case

- `\C` force case

- doesn’t matter in the beginning or at the end

- `smartcase` be smart

#### 73. Use the \v Pattern Switch for Regex Searches

- `:h /character-classes`

#### 74. Use the \V Literal Switch for Verbatim Searches

#### 75. Use Parentheses to Capture Submatches

- `\{num}` to ref the group

#### 76. Stake the Boundaries of a Word

- `<word>`  < and > are the word boundaries

- `*` `#` `g*` `g#`

#### 77. Stake the Boundaries of a Match

- `\vPractice \zsVim\ze is good` search for all but highlight Vim only

- positive lookaround

- negative lookaround

#### 78. Escape Problem Characters

- `=escape(@u, getcmdtype().’\’)` preprocess u register

### Search

### Substitution

### Global Commands

## Tools

### Index and Navigate Source Code with ctags

### Compile code and Navigate Errors with the Quickfix List

### Search Project-Wide with grep, vimgrep and Others

### Dial X for Autocompletion

### Find and Fix Typos with Vim’s Spell Checker

### Now What?

## Customize Vim to Suit Your Preferences

