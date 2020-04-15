To minimize the chance of permissions errors, you can configure npm to use a different directory. In this example, it will be a hidden directory on your home folder.

Make a directory for global installations:
```sh
 mkdir ~/.npm-global
```

Configure npm to use the new directory path:
```sh
 npm config set prefix '~/.npm-global'
```
Open or create a ~/.bash_profile file and add this line:

```sh
 export PATH=~/.npm-global/bin:$PATH
```

Back on the command line, update your system variables:
```sh
 source ~/.bash_profile
```
Test: Download a package globally without using sudo.
```sh
npm install -g jshint
```

If still show permission error run (mac os):
```sh
sudo chown -R $USER ~/.npm-global   
```

Credit: https://www.ideagital.com/watcharapron/แก้ปัญหา-missing-write-access-to-usr-local-lib-node-modules-npm-node-modules
