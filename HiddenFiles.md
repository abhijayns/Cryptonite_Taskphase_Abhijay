#**Comprehending Commands**

##**Hidden Files**

Found the hidden dot-prepended file using _ls -a_ command  

_hacker@commands-hidden-files:~/Desktop$ cd /_

_hacker@commands~hidden-files:/$ ls -a_

_. .dockerenv bin challenge etc lib lib64 media nix proc run srv tmp var_

_.. .flag-6969276282698 boot dev home lib32 libx32 mnt opt root sbin sys usr_

_hacker@commands~hidden-files:/$ grep pwn.college /.flag-6969276282698_
