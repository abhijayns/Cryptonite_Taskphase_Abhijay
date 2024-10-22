# Shell Variables

## Printing Variables

I printed out the _FLAG_ variable using _echo_ by prepending the variable name with _$_.

    hacker@variables-printing-variables:~$ echo $FLAG
    pwn.college{0oEX-FEUqdTT5WdXiAeP_afPOQ5.ddTN1QDL1cTN0czW}

## Setting Variables

I had set the PWN variable to the value COLLEGE.

    hacker@variables-setting-variables:~$ PWN=COLLEGE
    You've set the PWN variable properly! As promised, here is the flag:
    pwn.college{8kNzHa2Cxmp0cUmvZ4XvzvqIAZB.dlTN1QDL1cTN0czW}

## Multi-word Variables

I had set the variable PWN to COLLEGE YEAH.

    hacker@variables-multi-word-variables:~$ PWN="COLLEGE YEAH"
    You've set the PWN variable properly! As promised, here is the flag:
    pwn.college{cbYnuIgapUFYShiD222jA-J_Lmd.dBjN1QDL1cTN0czW}

## Exporting Variables

I invoked /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported.

    hacker@variables-exporting-variables:~$ export PWN=COLLEGE
    You've set the PWN variable to the proper value!
    hacker@variables-exporting-variables:~$ COLLEGE=PWN
    You've set the PWN variable to the proper value!
    You've set the COLLEGE variable to the proper value!
    hacker@variables-exporting-variables:~$ /challenge/run
    CORRECT!
    You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
    job! Here is your flag:
    pwn.college{osneIDa0SKXyQIV7er_gmm-8Rmk.dJjN1QDL1cTN0czW}
    You've set the PWN variable to the proper value!
    You've set the COLLEGE variable to the proper value!

## Printing Exported Variables

I invoked /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported and printed the exported variable using env command.

    hacker@variables-printing-exported-variables:~$ export PWN=COLLEGE

    hacker@variables-printing-exported-variables:~$ COLLEGE=PWN

    hacker@variables-printing-exported-variables:~$ env

    SHELL=/run/dojo/bin/bash

    HOSTNAME=variables~printing-exported-variables

    PWN=COLLEGE

    PWD=/home/hacker
    
    DOJO_AUTH_TOKEN=290d0c913e11cf01fe200b12955be464cbad72fa8c37def2d6389dea9272ce5d
    
    HOME=/home/hacker

    LANG=C.UTF-8

    LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=00:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.7z=01;31:*.ace=01;31:*.alz=01;31:*.apk=01;31:*.arc=01;31:*.arj=01;31:*.bz=01;31:*.bz2=01;31:*.cab=01;31:*.cpio=01;31:*.crate=01;31:*.deb=01;31:*.drpm=01;31:*.dwm=01;31:*.dz=01;31:*.ear=01;31:*.egg=01;31:*.esd=01;31:*.gz=01;31:*.jar=01;31:*.lha=01;31:*.lrz=01;31:*.lz=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.lzo=01;31:*.pyz=01;31:*.rar=01;31:*.rpm=01;31:*.rz=01;31:*.sar=01;31:*.swm=01;31:*.t7z=01;31:*.tar=01;31:*.taz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tgz=01;31:*.tlz=01;31:*.txz=01;31:*.tz=01;31:*.tzo=01;31:*.tzst=01;31:*.udeb=01;31:*.war=01;31:*.whl=01;31:*.wim=01;31:*.xz=01;31:*.z=01;31:*.zip=01;31:*.zoo=01;31:*.zst=01;31:*.avif=01;35:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.webp=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;3:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:*~=00;90:*#=00;90:*.bak=00;90:*.crdownload=00;90:*.dpkg-dist=00;90:*.dpkg-new=00;90:*.dpkg-old=00;90:*.dpkg-tmp=00;90:*.old=00;90:*.orig=00;90:*.part=00;90:*.rej=00;90:*.rpmnew=00;90:*.rpmorig=00;90:*.rpmsave=00;90:*.swp=00;90:*.tmp=00;90:*.ucf-dist=00;90:*.ucf-new=00;90:*.ucf-old=00;90:

    FLAG=pwn.college{Er-_AXrAERMQCJVqfjHDRu63orU.dhTN1QDL1cTN0czW}

    LESSCLOSE=/usr/bin/lesspipe %s %s

    TERM=xterm

    LESSOPEN=| /usr/bin/lesspipe %s

    SHLVL=1

    LC_CTYPE=C.UTF-8

    PATH=/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin=/run/workspace/bin/env_

## Storing Command Output

I read the output of the /challenge/run command directly into a variable PWN and printed PWN.

    hacker@variables-storing-command-output:~$ PWN=$( /challenge/run )

    Congratulations! You have read the flag into the PWN variable. Now print it out and submit it!

    hacker@variables-storing-command-output:~$ echo $PWN
    pwn.college{ItY_P9rqRx6a_qS0HjM8pbBrPSN.dVzN0UDL1cTN0czW}

## Reading Input

I used read command to set the PWN variable to the value COLLEGE.

    hacker@variables-reading-input:~$ read PWN COLLEGE
    You've set the PWN variable properly! As promised, here is the flag:
    pwn.college{AM6U-zbtspq6QpKL-hZr_pPpj47.dhzN1QDL1cTN0czW}

## Reading Files

I used read command to read /challenge/read_me into the PWN environment variable.

    hacker@variables-reading-files:~$ read PWN < /challenge/read_me
    You've set the PWN variable properly! As promised, here is the flag:
    pwn.college{ENquGh4ukRbNWEPaanQ7Q3wP-XG.dBjM4QDL1cTN0czW}
    
