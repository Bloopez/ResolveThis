# DNS over HTTPS backdoor

This program grabs the DNS TXT record from a specified domain and executes the content via powershell.

## Features
AES Encryption - Command(payload) is encrypted in AES for delivery to the DNS TXT record

SSL Encryption - Retrieval of payload is through the HTTPS protocol

### Files & Functions

#### generator.go
Responsible for generating the payload


#### main.go
Responsible for retrieving and executing the payload from DNS TXT record



## How to build/use

>**_NOTE:_** So far this only works with windows.

To use, replace the domain in the main.go file with your domain and run 
`GOOS=windows GOARCH=amd64 go build main.go`
to compile the executable.

Be sure to input your command in the generator.go file within `CmdContent`



