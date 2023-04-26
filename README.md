# go-cli

The goal is to understand how to write a cli app in Golang using Cobra. So the app will only print strings for sub-commands executions.

Say we are trying to build a simple go cli app. Which will have 2 sub-commands check-url and check-status. Both the commands will take a url/api as argument

PS E:\FRONTEND\go-cli-app\my-cli> .\my-cli.exe
url-monitor

Usage:
  url-monitor [command]

Available Commands:
  check-status check-status
  check-url    check-url
  completion   Generate the autocompletion script for the specified shell
  help         Help about any command

Flags:
  -h, --help   help for url-monitor

Use "url-monitor [command] --help" for more information about a command.
PS E:\FRONTEND\go-cli-app\my-cli> .\my-cli.exe check-url https://example.com/apis/v1/get-status 
HI!! From check-url sub-command with https://example.com/apis/v1/get-status as argument
PS E:\FRONTEND\go-cli-app\my-cli> .\my-cli.exe check-status https://example.com/apis/v1/get-status
HI!! From check-status sub-command with https://example.com/apis/v1/get-status as argument
PS E:\FRONTEND\go-cli-app\my-cli> .\my-cli.exe check-status example.com/apis/v1/get-status        
time="2023-04-26T15:45:23+05:30" level=fatal msg="wrong url type [parse \"example.com/apis/v1/get-status\": invalid URI for request]"      
PS E:\FRONTEND\go-cli-app\my-cli> git status
fatal: not a git repository (or any of the parent directories): .git
PS E:\FRONTEND\go-cli-app\my-cli> git add .
fatal: not a git repository (or any of the parent directories): .git
PS E:\FRONTEND\go-cli-app\my-cli> git remote add origin https://github.com/dev-soubhagya/go-cli.git
fatal: not a git repository (or any of the parent directories): .git
PS E:\FRONTEND\go-cli-app\my-cli> 
