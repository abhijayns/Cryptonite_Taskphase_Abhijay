#**Chaining Commands**

##**Your First Shell Script**

I had to research on how to write inside of a shell as nothing was working and I couldn’t solve the question. The source which I refered is  <https://cloudxlab.com/assessment/displayslide/63/writing-first-shell-script>. Reading the website, I learnt that the nano command had to be used to write inside of a shell and exit the shell with the key combination Ctrl+X and save the text. So firstly, I created a shell script using the touch command, then I used nano command to enter into the shell and wrote the two commands which were supposed to be written and then used the bash command and got the flag.

_hacker@chaining-your-first-shell-script:~$ bash_

_Please name your script with an '.sh' extension. This isn't strictly necessary_

_eventually, but we'll keep things explicit for the next few levels._

_hacker@chaining-your-first-shell-script:~$ touch x.sh_

_hacker@chaining-your-first-shell-script:~$ nano x.sh_

_hacker@chaining-your-first-shell-script:~$ bash x.sh_

_Great job, you've written your first shell script! Here is the flag:_

_pwn.college{0OJTOmvMXDXxYwbs2JLTMXMc21P.dFzN4QDL1cTN0czW}_
