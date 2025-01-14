# About 
The file **strong_aliases** contains bash functions and aliases. That are include in the .bashrc, to quickly perform daily tasks in the console.

# Manual
Main function **cli** show a list of available functions. Each function displays help when launched.
-  ctl             :  System  Toolkit 
-  sql             :  Mysql   Toolkit
-  log             :  Logs    Toolkit 
-  ngx             :  Nginx   Toolkit
-  dsk             :  Disk    Toolkit
-  net             :  Network Toolkit
-  note            :  Network txt viewer

# Install

#### Software requirements (optional)
```
apt install -y ccze tmux tar gunzip unzip rsync smartctl
```

#### One command launch
```
curl https://raw.githubusercontent.com/circlehook/bash-strong-cli/refs/heads/main/install.sh | bash && source ~/.bashrc && cli
``` 
#### Manual install 
```
wget -q -O - https://raw.githubusercontent.com/circlehook/bash-strong-cli/refs/heads/main/strong_aliases > ~/.strong_aliases
grep -q "strong_aliases" ~/.bashrc || echo "[ -f ~/.strong_aliases ] && . ~/.strong_aliases" >> ~/.bashrc
source ~/.bashrc
```
#### Usage
```
cli
```

# Pretty launch on your domain

#### Create a file cli.sh in the root of the site
```
#!/bin/bash

wget -q -O - https://raw.githubusercontent.com/circlehook/bash-strong-cli/refs/heads/main/strong_aliases > ~/.strong_aliases
grep -q "strong_aliases" ~/.bashrc || echo "[ -f ~/.strong_aliases ] && . ~/.strong_aliases" >> ~/.bashrc
```

#### One command launch
```
curl https://example.com/cli.sh | bash && source ~/.bashrc && cli
```

# Uninstall
To uninstall aliases, run:
```
cli drop
```
#### Manual uninstall
Remove row from .bashrc and delete file .strong_aliases 
```
nano /root/.bashrc
rm /root/.strong_aliases
source ~/.bashrc
```