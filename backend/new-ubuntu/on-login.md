# on Login

**To run some stuff every time you login to SSH shell, `mv` this file into  `~/.zprofile`**

```text
#
# Node Version Manager
#
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

#
# SSH - first, `scp ~/.ssh/newssh root@18.217.8.193:~/.ssh/newssh`
#
eval $(ssh-agent -s);
ssh-add ~/.ssh/newssh;

#
# hints
#
echo '
    NGINX:
    sites-available: $(ls /etc/nginx/sites-available)
    sites-enabled: $(ls /etc/nginx/sites-enabled)
';

#
# node
#
pm2 list
```

 

