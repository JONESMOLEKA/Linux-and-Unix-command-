The wget command in Linux is a command used to download files from the web. This command uses the URL of a file to download it. The command can be used to download data over HTTP, FTP, and HTTPS protocols.

**syntax**
```
wget [option] [URL]
```

Option	|Effect
--------|------
-h	|This option is used to display the help message for the wget command. It includes all the possible options which can be used with the wget command in Linux
-b	|This option is used to send the download process to the background as soon as it is initiated with the wget command. It frees up your terminal session to run other commands.
-i	|This option is used to read the URL for the wget command from a file. It eliminates the need for the wget command to have an URL and allows the inclusion of an input file. 
-o	|Name of the output file if you do not want the same name as the server has provided
-c	|This tag makes wget keep a track of the download progress in case of download interruptions. We can continue an interrupted download if this option was used when the download was initiated.
-tries=n	|This option is used to limit the number of tries for the wget command. Using this command will cause the wget utility to retry a download only ‘n’ times. The default is 20.
-limit-rate=maxlim	|This option is used to limit the download speed for the wget command. This helps the user to dictate the amount of bandwidth to be allocated for a download.

**Example**
- wget https://updates.jenkins-ci.org/download/war/2.277/jenkins.war
