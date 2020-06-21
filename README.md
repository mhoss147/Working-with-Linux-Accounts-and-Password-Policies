# Working-with-Linux-Accounts-and-Password-Policies

- Ubuntu server. The security-related changes are listed below:


      Update password settings to force the minimum password length to be 12 characters, 
      
      set the minimum password age to 3 days, and set the maximum password age to 180 days.
      
      Configure the accounts to lock out after 3 failed login attempts and to lock out for 10 minutes. 
      
      Do not include the root user account in the account lockout settings.

      You've also been tasked with setting up a temporary user account called contractor1 that will expire one week from today.

      Connecting to the lab:

      Use VNC on your computer to connect to the public IP address of the instance on port 5901 (x.x.x.x:5901).
      Log in with the username and password generated by the lab. Now use the "Guide" located above the video to view the scenario and tasks to be completed.

- Set up password requirements on a Linux host:

Set the minimum password length to 12 characters:

    Run the command sudo nano /etc/pam.d/common-password.
    
    At the end of the first uncommented line (line 25) add minlen=12, one space after sha512.
    
    Save the file and exit nano.

Set the maximum password age to 180 days and the minimum password age to 3 days:

    Run the command sudo nano /etc/login.defs.
    
    Search for 99999 (press Ctrl + W to search).
    
    Replace 99999 with 180.
    
    On the next line down, replace the 0 with 3.
    
    Save the file and exit nano.


# -----------------------------------------



# to see inside of a dir

    cloud_user@sorowar0073c:~$ ls -l "directoryName"

    cloud_user@sorowar0073c:~$ ls -l      (only long listing)

# to see contents of a directory recursively ( define the operation step by step)

    cloud_user@sorowar0073c:~$ ls -R "directoryName"


# to see most recent at the top 

    cloud_user@sorowar0073c:~$ ls -lt


# human readable

    $ ls -lh
    
    
# find the location of a cmd

cloud_user@sorowar0073c:~$ which ls


# list all environment variables

$ env


# PRINT the contents of path environment variable

cloud_user@sorowar0073c:~$ echo $PATH

cloud_user@sorowar0073c:~$ echo $HOME


# single (.) before file tells that it is in home directory and double (..) tells one dir up

cloud_user@sorowar0073c:~$ ls -a

.              .bash_history  .config  .lesshst  .ssh                      

..             .bash_logout


# ./fileName tells bash to execute something in that directory


./hello.sh == /home/user/hello.sh



# move a file to another directory

cloud_user@sorowar0073c:~$ mv "fileNameYouWantToMove" "derectoryNameWhereYouWantToMove"



# dislplay the name of the system kernel

$ uname


# kernel's release number

$ uname -r


# kernel's build date

$ uname -v


# name of the os

$ uname -o


# machine/processor type

$ uname -m

$ uname -p


# everthing ALL together

$ uname -a


# current working directory

$ pwd


# go to home directory from any level

$ cd    or    cd ~





# go back to LAST directory

$ cd -


# your ALL command history saved in hidden .bash_history

$ ls -a

$ cat .bash_history


# see command history in .bash_history with line numbered

$ history


# re-run the command from history with 

$ !historyNumber



# how many lines of command to save in history

$ echo $HISTFILESIZE









