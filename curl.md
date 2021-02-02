curl is an command line tool for transferring data between two servers. Other than downloading files curl also used to performs multiple tasks by the applications, services etc. Curl supported a verity of protocols (DICT, FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, MQTT, POP3, POP3S, RTMP, RTMPS, RTSP, SCP, SFTP, SMB, SMBS, SMTP, SMTPS, TELNET and TFTP) for file transferring.

In other words ....

curl is a command line tool to transfer data to or from a server, using any of the supported protocols (HTTP, FTP, IMAP, POP3, SCP, SFTP, SMTP, TFTP, TELNET, LDAP or FILE). curl is powered by Libcurl. This tool is preferred for automation, since it is designed to work without user interaction. curl can transfer multiple file at once.

**Syntax:**
```
curl [options] [URL...]
```

**Example:** Open a terminal on your system and type:

```
curl https://tecadmin.net
```

You will see the website content on terminal. This is the most basic uses of curl command line.

**URL Syntax**

The URL syntax is completely protocol-dependent with cURL. Before reading more about parameters or example, you must know the URL formats, you can use with curl.

* Use braces and quotes to define multiple URLs in single. Here braces expands to multiple urls. For example:
 ```
 "http://www.{one,two,three}.com"
```
Becomes, http://www.one.com, http://www.two.com and http://www.three.com.

* You can also define a range by using [] as in:
```
  "ftp://ftp.example.com/file[1-100].txt"
  "http://ftp.example.com/file[a-z].txt"
```
* You can also specify to use every N’th letter or number from a defined range.
```  
"ftp://ftp.example.com/file[1-100:5].txt"
  "http://ftp.example.com/file[a-z:2].txt"
```
Here the first url will refer to every 5’th file and second url with refer to every second letter.

CURL Command Options

curl command comes with large number of command line options. Which provides it great flexibility to perform various tasks. Here we will describe you some frequently used command options with curl command.

-s or --silent – While using this option, the command runs silently in background. No progress will be displayed on screen. Only the command result will be displayed.
curl -s http://www.example.com 
-O – The capital letter “O” is used to download a file using curl command. The filename will remain same on local system as on remote.
curl -O http://www.example.com/backup.zip 
-o or --output FILE – Use this option to write all data to file instead of displaying at standard output.
curl -o file.txt http://www.example.com 
While downloading a file, use this option to save file on local machine with provided name.

curl -o local.zip http://www.example.com/remote.zip 
-I or --head – Use this option to view the document information only. This will not download the content or file from server.
This is also useful to view header only details for a domain.

curl -I http://www.example.com 
-u or --user – Use this option to send authentication details with curl request. It is useful to download files from authenticated ftp server or web servers.
curl -u "username:password" -O ftp://ftp.example.com/remote.zip 
-T – curl also allows you to upload a file to remote ftp server. To upload a file use -T option followed by the local file name. If the remote server required authentication, make sure to provide authentication details with “-u” option.
curl -u ftpuser:ftppassword -T localfile.zip ftp://ftp.example.com/files/ 
-x or -–proxy – You can route your curl request via a proxy server. You can define proxy server with -x option.
curl -x some.proxy.com:3128 http://www.example.com 