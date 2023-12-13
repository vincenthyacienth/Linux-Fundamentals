# Linux-Fundamentals
## What Is a Linux Command?
A Linux command is a program or utility that runs on the command line. A command line is an interface that accepts lines of text and processes them into instructions for your computer.
Any graphical user interface (GUI) is just an abstraction of command-line programs. For example, when you close a window by clicking on the “X,” there’s a command running behind that action.
A flag is a way we can pass options to the command you run. Most Linux commands have a help page that we can call with the flag -h. Most of the time, flags are optional.
An argument or parameter is the input we give to a command so it can run properly. In most cases, the argument is a file path, but it can be anything you type in the terminal.
You can invoke flags using hyphens (-) and double hyphens (--), while argument execution depends on the order in which you pass them to the function.

## The 25 Most-Used Linux Commands
1. **ls Command**
`ls` is probably the first command every Linux user typed in their terminal. It allows you to list the contents of the directory you want (the current directory by default), including files and other nested directories.
`ls`

2. **Aias Command**
The `alias` command lets you define temporary aliases in your shell session. When creating an alias, you instruct your shell to replace a word with a series of commands.
For example, to set ls to have color without typing the --color flag every time, you would use:
`alias ls="ls --color=auto"`
As you can see, the `alias` command takes one key-value pair parameter: `alias NAME="VALUE"`. Note that the value must be inside quotes.
If you want to list all the aliases you have in your shell session, you can run the `alias` command without argument.
`alias`

3. **Unalias Command**
As the name suggests, the `unalias` command aims to remove an alias from the already defined aliases. To remove the previous ls `alias`, you can use:
`unalias ls`

4. **pwd Command**
The `pwd` command stands for “print working directory,” and it outputs the absolute path of the directory you’re in. For example, if your username is “john” and you’re in your Documents directory, its absolute path would be: /home/john/Documents.
To use it, simply type `pwd` in the terminal:
`pwd`

5. **cd Command**
The `cd` command is highly popular, along with ls. It refers to “change directory” and, as its name suggests, switches you to the directory you’re trying to access.
For instance, if you’re inside your Documents directory and you’re trying to access one of its subfolders called Videos, you can enter it by typing:
`cd Videos`

You can also supply the absolute path of the folder:
`cd /home/kinsta/Documents/Videos`

There are some tricks with the `cd` command that can save you a lot of time when playing around with it:
1) Go to the home folder
`cd`
2) Move a level up
`cd ..`
3) Return to the previous directory
`cd -
`
6. **cp Command**
It’s so easy to copy files and folders directly in the Linux terminal that sometimes it can replace conventional file managers.
To use the `cp` command, just type it along with the source and destination files:
`cp file_to_copy.txt new_file.txt`

You can also copy entire directories by using the recursive flag:
`cp -r dir_to_copy/ new_copy_dir/`

Remember that in Linux, folders end with a forward slash (/).

7. **rm Command**
Now that you know how to copy files, it’ll be helpful to know how to remove them.
You can use the `rm` command to remove files and directories. Be careful while using it, though, because it’s very difficult (yet not impossible) to recover files deleted this way.
To delete a regular file, you’d type:
`rm file_to_copy.txt`

If you want to delete an empty directory, you can use the recursive (-r) flag:
`rm -r dir_to_remove/`

On the other hand, to remove a directory with content inside of it, you need to use the force (-f) and recursive flags:
`rm -rf dir_with_content_to_remove/`

**Info**
Be careful with this — you can erase a whole day of work by misusing these two flags!

8. **mv Command**
You use the `mv` command to move (or rename) files and directories through your file system.
To use this command, you’d type its name with the source and destination files:
`mv source_file destination_folder/`
`mv command_list.txt commands/`

To utilize absolute paths, you’d use:
`mv /home/kinsta/BestMoviesOfAllTime ./`
…where `./` is the directory you’re currently in.

You also can use mv to rename files while keeping them in the same directory:
`mv old_file.txt new_named_file.txt`

9. **mkdir Command**
To create folders in the shell, you use the `mkdir` command. Just specify the new folder’s name, ensure it doesn’t exist, and you’re ready to go.
For example, to make a directory to keep all of your images, just type:
`mkdir images/`

To create subdirectories with a simple command, use the parent (-p) flag:
`mkdir -p movies/2004/`

10. **man Command**
Another essential Linux command is `man`. It displays the manual page of any other command (as long as it has one).
To see the manual page of the mkdir command, type:
`man mkdir`

11. **chmod Command**
The `chmod` command lets you change the mode of a file (permissions) quickly. It has a lot of options available with it.
The basic permissions a file can have are:
r (read)
w (write)
x (execute)
One of the most common use cases for `chmod` is to make a file executable by the user. To do this, type `chmod` and the flag `+x`, followed by the file you want to modify permissions on:
`chmod +x script`

You use this to make scripts executable, allowing you to run them directly by using the `./` notation.

12. **exit Command**
The `exit` command does exactly what its name suggests: With it, you can end a shell session and, in most cases, automatically close the terminal you’re using:
`exit`

13. **sudo Command**
This command stands for “superuser do,” and it lets you act as a superuser or root user while you’re running a specific command. It’s how Linux protects itself and prevents users from accidentally modifying the machine’s filesystem or installing inappropriate packages.
`Sudo` is commonly used to install software or to edit files outside the user’s home directory:
`sudo apt install gimp`
`sudo cd /root/`
 
It’ll ask you for the administrator’s password before running the command you typed after it.

14. **ping Command**
`ping` is the most popular networking terminal utility used to test network connectivity. `ping` has a ton of options, but in most cases, you’ll use it to request a domain or IP address:
`ping google.com`
`ping 8.8.8.8`

15. **vim Command**
`vim` is a free and open source terminal text editor that’s in used since the ’90s. It lets you edit plain text files using efficient keybindings.
Some people consider it difficult to use — exiting `Vim` is one of the most-viewed StackOverflow questions — but once you get used to it, it becomes your best ally in the command line.
To fire up Vim, just type:
`vim`

16. **history Command**
If you’re struggling to remember a command, `history` comes in handy. This command displays an enumerated list with the commands you’ve used in the past:
`history`

17. **passwd Command**
`passwd` allows you to change the passwords of user accounts. First, it prompts you to enter your current password, then asks you for a new password and confirmation.
It’s similar to any other change of password you’ve seen elsewhere, but in this case, it’s directly in your terminal:
`passwd`

Be careful while using it — you don’t want to mess up your user password!

18. **which Command**
The `which` command outputs the full path of shell commands. If it can’t recognize the given command, it’ll throw an error.
For example, we can use this to check the binary path for Python and the Brave web browser:
`which python`
`which brave`

19. **less Command**
`less` (opposite of more) is a program that lets you inspect files backward and forward:
`less large_text_file.txt`

The neat thing about `less` is that it includes more and vim commands in its interface. If you need something more interactive than `cat`, `less` is a good option.

20. **tail Command**
Similar to `cat`, `tail` prints the contents of a file with one major caveat: It only outputs the last lines. By default, it prints the last 10 lines, but you can modify that number with `-n`.
For example, to print the last lines of a large text file, you’d use:
`tail long.txt`

To view only the last four lines:
`tail -n 4 long.txt`

The `tail` command displaying the last four lines of a file.

21. **head Command**
This one is complementary to the `tail` command. `head` outputs the first 10 lines of a text file, but you can set any number of lines you want to display with the `-n` flag:
`head long.txt`
`head -n 5 long.txt`

22. **grep Command**
`Grep` is one of the most powerful utilities for working with text files. It searches for lines that match a regular expression and print them:
`grep "linux" long.txt`

You can count the number of times the pattern repeats by using the `-c` flag:
`grep -c "linux" long.txt`

23. **whoami Command**
The `whoami` command (short for “who am i”) displays the username currently in use:
`whoami`

24. **whatis Command**
`whatis` prints a single-line description of any other command, making it a helpful reference:
`whatis python`

25. wc Command
`Wc` stands for “word count,” and as the name suggests, it returns the number of words in a text file:
`wc long.txt`
`37 207 1000 long.txt`
    
Let’s breakdown the output of this command:
37 lines
207 words
1000 byte-size
The name of the file (long.txt)
If you only need the number of words, use the -w flag:
`wc -w long.txt`
`207 long.txt`
