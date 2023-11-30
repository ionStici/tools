[&larr; Back](./README.md)

# Redirecting Input / Output

Through **redirection** you can direct input and output of a command to and from other files and programs, and chain commands together in a pipeline.

- _"standard input"_ - abbreviated as **stdin** - is information inputted into the terminal through the keyboard or input device.
- _"standard output"_ - abbreviated as **stdout** - is the information outputted after a process is run.
- _"standard error"_ - abbreviated as **stderr** - is an error message outputted by a failed process.

How does redirection work? e.g. `echo "Hello" > hello.txt` The `>` command redirects the standard output to a file. Here, "Hello" is entered as standard input, and is then redirected to the file "hello.txt" by `>`. If the file "hello.txt" doesn't exists when you use this command, then it will create it.

<br>

## `>`

`>` takes the standard output of the command on the left, and redirects it to the file on the right.

`cat hello.txt > file.txt`

Here, the standard output of `cat hello.txt` is redirected to `file.txt`

Consider that `>` will overwrite all original content in "file.txt"

<br>

## `>>`

`cat hello.txt >> file.txt`

`>>` takes the standard output of the command on the left and appends (add) it to the file on the right.

Above, the content of "hello.txt" will be added to "file.txt" without changing its original content.

<br>

## `<`

`cat < hello.txt`

`<` takes the standard input from the file on the right and inputs it into the program on the left.

Above, "hello.txt" is the standard input for the `cat` command, the standard output appears in the terminal.

<br>

## `|`

`|` is a **pipe**, it takes the standard output of the command on the left, and _pipes_ it as standard input to the command on the right. This of this as _"command to command"_ redirection.

- `cat hello.txt | wc`

  Here, the output of `cat hello.txt` becomes the standard input to the `wc` command. In turn, `wc` (word count) command outputs the number of lines / words / characters from "hello.txt" file.

- `cat < hello.txt | wc | cat >> hello.txt`

  Multiple `|` can be chained together. Here, the standard output of `cat < hello.txt` is piped to `wc`, then the standard output of `wc` is piped to `cat`, which redirects the standard output to "hello.txt".

<br>

## `sort`

`sort hello.txt`

`sort` takes the standard input and orders it alphabetically for the standard output (it doesn't change the file itself).

`cat hello.txt | sort > sortedHello.txt`

Here, the command takes the standard output from `cat hello.txt` and pipes it to `sort`, which in turn redirects the output to a new file named "sortedhello.txt".

<br>

## `uniq`

`uniq` stands for **unique**, it filters out adjacent, duplicate lines in a file.

- `uniq hello txt`

Consider: only adjacent up and down duplicates are removed, rest duplicated will remain. To fix this, we can first sort them, and only then remove duplicates:

- `sort hello.txt | uniq | cat`

  By piping `sort hello.txt` to `uniq`, all duplicate lines are alphabetized (and thereby made adjacent) and filtered out.

<br>

## `grep`

`grep` stands for **“global regular expression print”**. It searches files for lines that match a pattern and then returns the results. It is case sensitive.

- `grep Hello file.txt` // returns "Hello" if matched

  Here, `grep` searched for anything that matched "Hello" in "file.txt"

- `grep -i hello file.txt` The `-i` option enables `grep` to be case insensitive.

- `grep -R hello /Users/Mac/Desktop/folder` returns _/Users/Mac/Desktop/folder/file.txt:Hello_

  `grep -R` searches all files in a directory and outputs filenames and lines containing matched results.

- `grep -Rl Hello /Users/Mac/Desktop/folder` returns _/Users/Mac/Desktop/folder/file.txt_

  `grep -Rl` searches all files in a directory and outputs only filenames with matched results (no lines).

Note that we don't use quotes for the string argument in our command.

<br>

## `sed`

`sed` stands for **stream editor**. It accepts standard input and modifies it based on an expression, before displaying it as output data.

- `sed 's/snow/rain/' file.txt`

  `s` stands for "substitution". It is always used when using `sed` for substitution.

  `snow` the search string, or the text to find.

  `rain` the replacement string, or the text to add in place.

  Here, `sed` searches 'file.txt' for the word "snow" and replaces it with "rain". Note that this command will replace only the first instance of "snow".

- `sed 's/snow/rain/g' file.txt`

  Here we use the `g` expression, meaning "global". `sed` will search "file.txt" for the word "snow" and will replace it with "rain" _"globally"_, this means all instances of "snow" in a file will be turned to "rain".

- `sed -i 's/snow/rain/g' file.txt`

  `sed` as we’ve used it will only rewrite the command line output and the actual file won’t be changed.

  To rewrite the actual file, we need to use the `-i` option.

<br>

## Review

**Redirection** reroutes standard input, standard output, and standard error.

_The common redirection commands are:_

- `>` redirects standard output of a command to a file, overwriting previous content.
- `>>` redirects standard output of a command to a file, appending new content to old content.
- `<` redirects standard input to a command.
- `|` redirects standard output of a command to another command.

_Useful commands when combined with redirection commands:_

- `sort` : sorts lines of text alphabetically.
- `uniq` : filters duplicate, adjacent lines of text.
- `grep` : searches for a text pattern and outputs it.
- `sed` : searches for a text pattern, modifies it, and outputs it.

<br>
