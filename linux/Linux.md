<style>
.highlight{
  color: #32CD32
}
.imp{
  color: #FF8080
}
.trivia{
  color: #E6D100
}
.header{
  color: #EE82EE
}
</style>

# <span class="header">Introduction to Linux</span>

Just like Windows, Mac or IOS, <span class="highlight">Linux an Operating System</span>. But What is an operating System ? What does it do ? And the answer is that, an Operating System (OS) is a bridge between the software and hardware  component of the the device. It manages all of the hardware resources associated with our desktop or laptop. Without an OS the device wouldn't function.

# Why use Linux ?

Until a few years ago, Linux was used mainly for servers and was not considered sutiable for desktops. But it's user-interface and ease of use has been steadily improving over the past few years. And Now, there are many reasons why Linux should be preferred over other software such as Windows or Mac. Given below are few of the reasons why.

* Simplified Update for all Software
  
  Maintaining the Linux OS is easy, as the user can centrally update the OS and all software installed very easily. All the variants of Linux have their own central software repository, which is used to update the system and keep it safe. They offer regular updates and the system can be updated without rebooting it . The updating can be done periodically, with just a few clicks, or users can even automate the updating process. Updating a Windows system is not so easy compared to a Linux system . Also, in Windows, all the third party software like Acrobat Reader and Firefox have to be updated individually.

  With Linux any app can be installed using a single command such as :

  <pre>
  <b>$ sudo yum install package</b><br>
  or<br>
  <b>$ sudo apt install package</b>
  </pre>

  Also, any app can be upgraded using commad such as :


  <pre>
  <b>$ sudo yum update</b><br>
  or<br>
  <b>$ sudo apt update</b> // This will update the repository 
  <b>$ sudo apt upgrade</b>  // This will update the app.
  </pre>

  To uninstall the app the command is as follows :

  <pre>
  <b>$ sudo yum remove package</b><br>
  or<br>
  <b>$ sudo apt remove package</b>
  </pre>

* Free Software Licensing

  Linux is Completely free and users do not need to pay for anything . All the basic software required by a user and even an advanced user are available. Even the equivalent of professional software for desktop pubblishing, photo editing, audio editing and video editing are available.

  This feature is especially useful for commercial organizations such as Schools, Businesses and I.T Companies. Compare it to Windows OS whose Basic version can costs upto Rs 9,299.00 and Pro version can cost upto Rs 22,799.00 for a single PC. Imagine, a Company (assuming to have atleast 10 employees) must spend a minimum of Rs 9,29,900.00 to get started.

  Extra :

  Now, to get around this some individuals install a pirated version of Windows and can get away with it, if it's a personal desktop. But Commerical companies won't use such measures since not only is it unethical but if the audit logs are checked and a Company is found using pirated OS, it can be fined heavily and the deivces can be siezed. To avoid all this hassle, all the companies simply opt to use Linux as their OS.

* Access to Open Source

  "Source code" is the part of software that most computer users don't ever see; it's the code computer programmers can manipulate to change how a piece of software—a "program" or "application"—works. Programmers who have access to a computer program's source code can improve that program by adding features to it or fixing parts that don't always work correctly.

  ## Extra
 
  This comes as shock to many people that 'Android' one of the most popular mobile operating system is based on Linux . But do not misunderstand what that line means. To put it simply, Android may be based on Linux, but it's not based on the type of Linux system that we use on PC i.e We cannot run Android apps on Linux and vice-versa. 

  So, What does it mean when we say 'Android is based on Linux'? Here, when we use the word 'Linux' we mean the 'Linux kernel' (A kernel is the core part of an OS)

# Baisc Linux Commands

| Commands |            Fullforms            |                                  Their Function                                   |
| :------: | :-----------------------------: | :-------------------------------------------------------------------------------: |
|    cd    |        Change Directory         |                  To navigate through Linux files and directories                  |
|    ls    |              List               |                        To view the contents of a directory                        |
|   cat    |           Concatenate           |           To list the contents of a file on the standard output (sdout)           |
|    cp    |              Copy               |         To copy files from the current directory to a different directory         |
|    mv    |              Move               |            To move files, although it can also be used to rename files            |
|    rm    |             Remove              |                To delete directories and the contents within them                 |
|   pwd    |      Print Work Directory       |           To find out the path of the current working directory(folder)           |
|  mkdir   |         Make Directory          |                              To make a new directory                              |
|  rmdir   |        Remove Directory         |                               To delete a directory                               |
|  touch   |                -                |                            To create a blank new file                             |
|  locate  |                -                |                                 To locate a file                                  |
|   find   |                -                |                     To locate a file within a given directory                     |
|   grep   | Global Regular Expression Print |               To let us search through all the text in a given file               |
|   sudo   |          SuperUser Do           |    Enables us to perform tasks that require administrative or root permissions    |
|    df    |            Disk Free            |                  Shows a report on the System's disk space usage                  |
|    du    |           Disk Usage            |                 To check how much space a file or directory takes                 |
|   head   |                -                |                    To view the first ten lines of a text file                     |
|   tail   |                -                |                     To view the last ten lines of a text file                     |
|   diff   |           Difference            |                  Compares the contents of two files line by line                  |
|   tar    |          Tape Archive           | To archive multiple files into a tarball(Linux file format similar to zip format) |
|  chmod   |           Change Mode           |    To change the read, write and execute permissions of files and directories     |
|  chown   |          Change Owner           |        To change or transfer the ownership of a file to specified username        |
|   jobs   |                -                |               To display all current jobs along with their statuses               |
|   kill   |                -                |                        To terminate unresponsive programs                         |
|   ping   |                -                |                     To check connectivity status to a server                      |
|   wget   |                _                |                     Used to donwload files from the internet                      |
|  uname   |            Unix Name            |               To print detailed information about our Linux system                |
|   top    |       Table of Proccesses       |     To display a list of running processes and how much CPU each process uses     |
| history  |                -                |                   To review the commands you've entered before                    |
|   man    |             Manual              |     To display the user manual of any command that we can run on the terminal     |
|   echo   |                -                |                           To move some data into a file                           |
|   zip    |                -                |                       To compress files into a zip archive                        |
|  unzip   |                -                |                  To extract the zipped files from a zip archive                   |
| hostname |                -                |                         To know the name of host/network                          |
| useradd  |                -                |                       To create a new user for Linux system                       |
| userdel  |                -                |                        TO delete a user from Linux system                         |

