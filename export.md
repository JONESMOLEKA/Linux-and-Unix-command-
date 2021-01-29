
The export command in Linux is used for creating environment variables. You can use it like this:

- `export myvar`
or a shorthand like this to assign it a value immediately:

- `export myvar=5`
You can see the value of exported variables with the echo command:

- `echo $myvar`
To make the changes permanent, you should add it to the ~/.bashrc file.