#**Perceiving Permissions**

##**Fun with Groups Names**

I used _id_ command to view the group and changed the group of _/flag_ to _grp20546_ using _chgrp_ command.

_hacker@permissions-fun-with-groups-names:~$ id_

_uid=1000(hacker) gid=1000(grp20546) groups=1000(grp20546)_

_hacker@permissions-fun-with-groups-names:~$ chgrp grp20546 /flag_

_hacker@permissions-fun-with-groups-names:~$ cat /flag_

_pwn.college{s8l9ij3jU21CdXKzn1nSg7P0RLb.dJzNyUDL1cTN0czW}_
