# Deno on Windows
I've found a way to enjoy Deno on Windows without the frustration of not being able to successfully run code examples from the Demo manuals or from the many helpful online blog-posts.

I've tried WSL2 on my old laptop, and it did allow me to run Deno examples.    
Unfortunately, WSL2 didn't play well day-to-day on my old laptop.

I've now found a way to have my cake and eat it too.  

I've discovered that the Bash shell installed by Git for Windows, can be set as the default terminal shell in VSCode.  This does not require WSL2 to be installed.   
This shell runs all of the example code in the Deno manual, with some very minor changes for OS-Signals.

The steps required are as follows:

## Git for Windows
Install Git for Windows.  
https://gitforwindows.org/

### Git BASH
Git for Windows provides a BASH emulation used to run Git from the command line. It is installed as part of the Git for Windows install.

### BASH as default
To set Git-Bash as the default terminal shell in VSCode:   

 - open settings in vscode  -- file -> preferences -> settings
 - search -> terminal.integrated.defaultProfile.windows
 - select "Git Bash"
 
 or in the json file:   
 ```
 "terminal.integrated.defaultProfile.windows": "Git Bash"
 ```
Now, whenever you open a new terminal in Code, it will default to BASH.

You can still open a new CMD or Powershell terminal from the drop-down in the top-right of the terminal pane.   

The Git-BASH shell even support `Shebang` files.

