# AWS_errors
## Connect with PuTTy: 
* Error `Server refused our key`\
:+1: Always recheck the instance user_name (from [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connection-prereqs.html), e.g. ec2-user, ubuntu,...etc) and your Public IPv4 DNS in the Instance details.\
Format: instance_user_name@Public_IPv4_DNS

## Reconnect with puTTy
* Error: after it connected once, I tried to connect again but this error `Network Error: Connection timed out` appeared\
:+1: At each time you stop/start the instance the public DNS changes so you have to update it each time on the **Host** box in puTTy.

## Connecting AWS with VSCode
Followed this [video](https://youtu.be/R7cUtQu7jww) untill the minute (1:30) then ran into an error
* Error: `process tried to write to a nonexistent pipe` preceded by `Garabage at the end of line..`\
:+1: I had spaces in the path of the `.pem` key, so I needed to copy it to another path without spaces and it worked

## Enabling bash debugger on vscode and aws machine
Followed this [link](https://marketplace.visualstudio.com/items?itemName=rogalmic.bash-debug)\
* Error: `try to reach unreachable code while setting environment`\
:+1: Check intallation of [WSL](https://www.windowscentral.com/install-windows-subsystem-linux-windows-10) before linux distros **and** enable **virtualization** on your PC through BIOS. 