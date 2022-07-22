# NVM Cheatsheet

## Install

- Check version to install

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
```

## Reference

```bash
nvm --help              # help!

nvm current             # show current installed version
nvm ls-remote           # list all available versions 

nvm ls                  # list locally installed versions 
nvm list

nvm version             # show current version

nvm which x.x.x         # path to the installed x.x.x version

nvm use x.x.x           # swap to and use version x.x.x

nvm install x.x.x       # install x.x.x 
nvm install --lts       # install latest
nvm install node        # install latest node - use node -v to check current

nvm uninstall Vx        # where x(.x.x) is the version to uninstall 

nvm alias default x.x.x # default a specific version
nvm alias default Vx    # specify latest installed major x version    
nvm alias default node  # use latest installed version of node
```