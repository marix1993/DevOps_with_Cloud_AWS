## How to make:
### - variable 
### - environmental variable
### - persistent environmental variable


1. First you have to create `instance` with `user data`.
2. Press `Launch instance` (top right corner) and follow the steps as usual.
3. Choose proper `security group`.
4. In `Advanced settings` go to `User data` and add few lines of script (make sure it's all correct,
   otherwise it won't work).

`#!/bin/bash`

`sudo apt update -y`

`sudo apt upgrade -y`

`sudo apt install nginx -y`

`sudo systemctl restart nginx`

`sudo systemctl enable nginx`

5. Now connect instance via `.ssh` and if everything went fine script
   should work properly (to check it we can use command : `sudo systemctl status nginx`).
6. To check available environments we can use command `printenv`.
7. To see more info about environments use `env`.
8. To check our current location use `printenv pwd` command.
9. To create `variable` use `variablename=valueofvariable`.
10. To see value of `variable` use `echo $variablename`.
11. To create `environmental variable` use `export variablename=valueofvariable`

### Unfortunately variables are not persistent (after closing the terminal they are gone). To fix this we need to source the bash environment.

1. First add variable to bash environment. To do that  use `sudo nano .bashrc`.
2. At the end of this file add `export variablename=variablename`.
3. `CTRL + s` to save, `CTRL + x` to close.
4. To reads and execute newly made command use `source .bashrc` command.
5. To check if everything works and `environmental variable` is persistent `exit`,
login again and run `printenv variablename`.
