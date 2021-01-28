The who command prints information about all users who are currently logged in.

**Syntax**

`who [ OPTION ]... [ FILE ] [ am i ]`


Options| Description 
-------|-------------
-a, --all	|Same as using the options -b -d --login -p -r -t -T -u.
-b, --boot	|Display the time of the last system boot.
-d, --dead	|Display dead processes.
-H, --heading	|Print a line of column headings.
--ips | Print IP addresses instead of hostnames. With --lookup, canonicalizes based on stored IP, if available, rather than stored hostname.
-l, --login	|Print system login processes.
--lookup	|Attempt to canonicalize hostnames via DNS.
-m	|Only print information about the user and host associated with standard input (the terminal where the command was issued). This method adheres to the POSIX standard.
-p, --process	|Print active processes spawned by init.
-q, --count	|Displays all login names, and a count of all logged-on users.
-r, --runlevel	|Print the current runlevel.
-s, --short	|Print only name, line, and time fields, which is the default.
-t, --time	|Print the last time the system clock was changed, if the information is available.
-T, -w, --mesg	|Add a character which indicates the state of the terminal line: "+" if the terminal is writable, "-" if it's not, or "?" if a bad line is encountered.
-u, --users	|Print the idle time for each user, and the process ID.
--message	|Same as -T.
--writable	|Same as -T.
--help	|Display a help message, and exit.
--version	|Display version information, and exit.