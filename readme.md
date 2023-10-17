## Happy Docker containers

There are 4 containers:

An application (1) with a TCP socket client that sends random strings (with only alpha chars) every 2 seconds to another application (2) with a TCP socket server, the application (2) sends the received data to another application (3) calling a web service, the application (3) receive the data through an exposed web service (http) and get the ASCII decimal value of the chars and if the sum is even insert the value to the even table of the database, if the value is odd the application (3) insert the value to the odd table, database has other tables that store the alpha strings and the OCT, HEX, BIN ASCII value of the strings.
Another web application (4) that requests the data to the application (3) via POST and the data are shown in a datatable.

## Services implemented

I implemented:

- [Python web service with MySQL as DB](https://github.com/DvdCp/python-web-service)
- [Javascript TCP/IP server](https://github.com/DvdCp/server-string-receiver)
- [Javascript TCP/IP client](https://github.com/DvdCp/client-string-sender)
- [Python http client](https://github.com/DvdCp/python-http-client)

Every projects has its own `readme.md` file with instructions to follow.

Docker is required because the projects are intented to be containers.
