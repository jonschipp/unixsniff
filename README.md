# unixsniff
Sniffer for unix sockets

Enable sniffing on socket
```
$ ./unixsniff start /var/run/docker.sock
> 2016/02/11 17:34:19.712096  length=89 from=0 to=88
 47 45 54 20 2f 76 31 2e 32 32 2f 63 6f 6e 74 61  GET /v1.22/conta
 69 6e 65 72 73 2f 6a 73 6f 6e 20 48 54 54 50 2f  iners/json HTTP/
 31 2e 31 0d 0a                                   1.1..
 48 6f 73 74 3a 20 0d 0a                          Host: ..
 55 73 65 72 2d 41 67 65 6e 74 3a 20 44 6f 63 6b  User-Agent: Dock
 65 72 2d 43 6c 69 65 6e 74 2f 31 2e 31 30 2e 30  er-Client/1.10.0
 20 28 6c 69 6e 75 78 29 0d 0a                     (linux)..
 0d 0a                                            ..
--
< 2016/02/11 17:34:19.726062  length=141 from=0 to=140
 48 54 54 50 2f 31 2e 31 20 32 30 30 20 4f 4b 0d  HTTP/1.1 200 OK.
 0a                                               .
 43 6f 6e 74 65 6e 74 2d 54 79 70 65 3a 20 61 70  Content-Type: ap
 70 6c 69 63 61 74 69 6f 6e 2f 6a 73 6f 6e 0d 0a  plication/json..
 53 65 72 76 65 72 3a 20 44 6f 63 6b 65 72 2f 31  Server: Docker/1
 2e 31 30 2e 30 20 28 6c 69 6e 75 78 29 0d 0a     .10.0 (linux)..
 44 61 74 65 3a 20 54 68 75 2c 20 31 31 20 46 65  Date: Thu, 11 Fe
 62 20 32 30 31 36 20 32 32 3a 33 34 3a 31 39 20  b 2016 22:34:19
 47 4d 54 0d 0a                                   GMT..
 43 6f 6e 74 65 6e 74 2d 4c 65 6e 67 74 68 3a 20  Content-Length:
 33 0d 0a                                         3..
 0d 0a                                            ..
 5b 5d 0a                                         [].
 ```
 
 Disable sniffing and restore socket
 `$ ./unixsniff stop /var/run/docker.sock`
