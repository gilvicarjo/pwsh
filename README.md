# Powershell Support Resources
This is a page where I put all the most used resources in my daily tasks with PowerShell

## to show only the local ports that are in the Listen state
Get-NetTCPConnection | Where-Object {$_.State -eq 'Listen'} | Select-Object LocalAddress,LocalPort

## to get a list of all TCP connections on the server and their associated ports
Get-NetTCPConnection | Select-Object LocalAddress,LocalPort,RemoteAddress,RemotePort,State
