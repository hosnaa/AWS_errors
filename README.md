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
:+1: If you've the .pem in D_drive, change to C_drive
:+1: Always check the configuration file is correctly written 

## Enabling bash debugger on vscode and aws machine
Followed this [link](https://marketplace.visualstudio.com/items?itemName=rogalmic.bash-debug) with all configurations\
* Error: `try to reach unreachable code while setting environment`\
:+1: Check intallation of [WSL](https://www.windowscentral.com/install-windows-subsystem-linux-windows-10) before linux distros **and** enable **virtualization** on your PC through BIOS. 

## Debug bash file that needs arguments/operands
:+1: instead of arguments placeholder '$0, $1, $2' write their equivalent strings; ".."

## Reactivate Conda environment in VSCode
:+1: Follow this [answer](https://stackoverflow.com/questions/43351596/activating-anaconda-environment-in-vscode) where the steps are: 
1. `ctrl + shift + p` on vscode, search for **select interpreter** 
2. Select the Anaconda environment (probably 1st env)

## Can't see a module that's definitely downloaded by (pip) and (sudo pip)
:+1: Re-check that you're selecting the python interpreter that you're installing at, and that you're standing at

## To get previous commands used in your linux (Reverse history)
- Press `ctrl + R`

## Unable to install pip while trying to make `sudo apt-get python-pip` 
- Followed the steps [here](https://exerror.com/unable-to-locate-package-python-pip/)
- `sudo apt-get install software-properties-common`
- `sudo apt-add-repository universe`
- `sudo apt-get update`
- `sudo apt-get install python-pip`
- `sudo apt-get install python2-pip` or `3` instead of `2`

## VSCode error while Installing libraries "Reload Required" even after reloading
- Need to install the latest version of vscode and have the same python interpreter version locally and remotely on vscode
