The Pipe is a command in Linux that lets you use two or more commands such that output of one command serves as input to the next. In short, the output of each process directly as input to the next one like a pipeline. The symbol '|' denotes a pipe.

**Example**
- cat file1 | cut -d '"' -f 1
- echo "testssgu" | grep "test"