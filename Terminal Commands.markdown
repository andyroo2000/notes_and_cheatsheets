# Terminal Commands

* `ctrl-l` = clear the window
* `ctrl-u` = clear the current line


## Flags

* `-i` = case insensitive
* `-or` = or
* `-and` = and

* `-ctime` = created time
* `-atime` = accessed time
* `-iname` = case insensitive name

* `2` = standard error output (i.e. `2>> to append`)

## Combinations

* `cat test.js` = prints the contents of the file "test.js"
* `find . -name "*.jpg"` = find files in the current directory that end in .jpg
* `find . -size +2048` = find files larger than 1MB
* `find . -size -2048` = find files smaller than 1MB
* `find . -mtime -1` = find files modified within the last day
* `find . -mtime +1` = find files modified more than a day ago

* `grep "hello" someFile.js` = shows lines containing "hello" inside "someFile.js"

* `echo "Hello World!" > someFile.js` = writes the text "Hello World!" to a file called "someFile.js"

* `ls fakefile 2> log` = writes the error message to a file called "log"
* `ls fakefile 2>> log` = appends the error message to a file called "log"

## Piping Combinations

* `ls -a | grep "\."` = pass the results of `ls-a` into the 'grep' command and return all of the files that start with a `.` (the period must be escaped)

