# JV 1.0
#### Description
Simple utility to compile and run java programs via one command.
#### Usage
`jv [-0cdhrs] [filename...]`
#### Options
`-c <filename...>: Compile only`<br>
`-r <filename>: Run precompiled class`<br>
`-h: Help message`<br>
`-s <filename>: Compile and run without deleting classes after execute`<br>
`-d: Compile all java files in current directory`<br>
`-0: Show only error messages`
#### Installation
When downloaded, run `bash jv` from the directory where is it located and it will create its' executable copy in `/usr/bin/`, then run `jv` from any place.
#### Useful info
* By default this utility compiles all *.java files in the current directory and then automatically finds main class to run. Just use `jv` wherever needed.
* Pass only filenames, without exstensions (.java, .class).
* When using the `-r` option, pass only the main class (which contains `public static void main(String[] args)`)
* Use the `-c` and `-d` options before `-r`, ex.: `jv -cr test`, `jv -dr test`. It's acceptable to pass more than one .java files, but the first one must be the main (read above).
* To disable success messages, warnings and notes use the `-0` option before other options, ex.: `jv -0`, `jv -0cr test`, `jv -0s test`
* Unfortunately, the utility **does not** currently support wildcards and directories as arguments.
