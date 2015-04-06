# Windows_environment
How to set up Window's Package Manager and Unix like command line




#Purpose

DevMountain recommends that students come to class with a macbook product during the span of the course.  The main reason for this is that Windows and IOS environments are built on fundamentally different architectures.  Most of our instructors and mentors work full time on Apple machines and oftentimes are unable to help students when issues occur on a Windows machine.  

We are sensitive, however, to the fact that some people may not have the resources to purchase a new machine.  Though we cannot eliminate all differences, the instructions that follow should help minimize the differences between Apple and Windows environments, especially as they relate to the first couple of weeks of class.


##Command Line

###[PowerShell](http://en.wikipedia.org/wiki/Windows_PowerShell)

Powershell is a more powerful version of cmd prompt that is native to windows.  Press the "windows" button and start typing powershell and hit enter to use it.  The commands are very different from those of Apple's "Terminal".  Using PowerWhell makes it confusing and difficult on the first few days when you are learning how to use the command line.

###[cmder](http://gooseberrycreative.com/cmder/)

This is a command line tool that was made to resemble the unix (same as apple) command line.  It doesn't contain ALL of the same commands, but it is very close and will be your best option to keep up during the first few days of class.  You can install it by FIRST installing chocolatey below, then running the following command in PowerShell (as an admin):

  choco install cmder


##Package Manager

###[Chocolatey](https://chocolatey.org/)
Chocolatey is Window's functional equivalent to **Apple's "Brew"**.  Chocolatey will allow you to easily download, update, or remove software directly from the command line interface with one simple command.  Example:

  choco install git

This short bit of code will automatically download, extract, install, and place pointers to the program so that you can access it directly from the command line like this:

  git pull

Programs can be just as easily removed:

  choco uninstall git

###Install Chocolatey

To install Chocolatey, you must first open up PowerShell as an administrator (by right clicking PowerShell Icon).  Paste in the following command:

  Set-ExecutionPolicy Unrestricted

Then paste and run the following:

  (iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1')))>$null 2>&1


This should install chocolatey on your machine.  If you have issues you can look at other download options  [here](https://github.com/chocolatey/choco/wiki/Installation).  Go to their website to see a list of the available packages [here](https://chocolatey.org/)

Note that you must be in PowerShell as an admin (by right clicking the icon) to download new packages.  Just remember that chocolatey will do the same thing that "Brew" does for a mac.  Here is a list of programs that you may eventually download via chocolatey:

- git
- sublimeText3
- cmder
- mySql
- nodejs
