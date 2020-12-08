These config files are for quick reference, whether to revert or to setup a new machine, this project will serve as a working outline of the process to setup a wsl2 development enviroment on a given windows system (assuming the system meets requirements found here: ```https://docs.microsoft.com/en-us/windows/wsl/compare-versions```). 

I had to do this out of desperation after my 2019 macbook air fought out of its weight class against a large, hot coffee. It turned out quite tragically but I thankfully found a gently-used used dell g7 on craigslist and rolled the dice. I couldnt be happier with the end result.

To setup wsl2 development enviroment:

Make sure to run any commands for windows-based apps though opening powershell as an administrator.

Install chocolatey package manager ```https://chocolatey.org/install```  for quick and easy installation of windows apps and programs such as windows-terminal and vscode(there is a plugin for vs code that recognizes when it is being run on the sub-system). Think of it as homebrew but with a less hip name. (you can still use homebrew if you really want to once you get set up in wsl2).

I immediatley then use chocolatey to install any programs such as aquasnap (shiftit but better) and 8gadgetpack. You can use it to install spotify and the like, so have at it.

One point of note to consider is whether you intend to develop primarily on the subsystem.  If you install dependencies into the traditional windows directories, packages like npm will run incredibly slowly when called on through the subsystem. To avoid this, you can wait to install what you will actually use to develop with until you've got your bash shell set up.

First, install wsl ```choco install wsl -y```. The -y flag will auto accept the questions that pop up through powershell, so only use this is if youre comfortable with that. After this, open the control panel, hit programs and hit 'Turn windows features on or off.'
From here, navigate down to windows subsystem for linux and activate it. you will also need to activate virtual machine platform if you intend to use wsl2(recommended). 

Your computer will restart. When it comes back, everything will be the same but the subsystem will have been activated. You can now ```choco install wsl2``` and upgrade, unless you have a reason you don't want to.

I chose to use ubuntu as my linux distribution due to its ease of use and setup. you can install via ```choco install wsl-ubuntu-2004```, or you can install traditionally through the microsoft store by searching for ubuntu.

After its finished downloading, open and install ubuntu. You will be asked for a unix username and password; you'll definitely want to remember these.  The first time you open ubuntu with windows terminal, youll be using the bash shell.

I have included an alias file with some simple aliases to get started. Your .bashrc file has built in support for using a .bash_aliases file if you want to consolidate and are planning on adding a lot of them. 

If you want to go full mac, zsh is available but after hours of experimentation, it was so much painfully slower than bash, regardless of the dependencies were, that I figured it wasnt worth the effort fixing something that wasnt broken. Many have been able to use it with no problems but zsh has confirmed they're aware of an issue affecting wsl2.

From here, the world, or subsystem, is your oyster. I choose to install using apt-get as this was designed for use with linux and has worked the most seamlessly for me. Also, as I mentioned above, its great, like homebrew, sans the hip name. 

If anyone does end up reading this, any feedback is much appreciated as I am still learning and want to make sure I am not suggesting anything dangerous or stupid. I'd also love to hear if there are any better ways to work. Thank you.

    

   
