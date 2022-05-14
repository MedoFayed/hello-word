A second extension to add is Black, which is a Python code formatter that has quickly
become the default within the Python community. To install Black, open a Terminal
window within VSCode by going to  Terminal -> New Terminal  at the top of the page.
In the new terminal window opened at the bottom of the page, type  python -m pip
install black . Next, open up the VSCode settings by navigating to  File ->
Preferences -> Settings  on Windows or  Code -> Preferences -> Settings  on
macOS. Search for “python formatting provider” and select  black  from the dropdown
options. Then search for “format on save” and enable “Editor: Format on Save”. Black will
now automatically format your code whenever a  *.py  file is saved.


Install Git
The final step is to install Git, a version control system that is indispensable to modern
software development. With Git you can collaborate with other developers, track all your
work via commits, and revert to any previous version of your code even if you accidentally
delete something important!
On Windows, navigate to the official website at  https://git-scm.com/  and click on the
“Download” link which should install the proper version for your computer. Save the file
and then open your Downloads folder and double click on the file. This will launch the Git
for Windows installer. Click the “Next” button through most of the early defaults as they
are fine and can always be updated later as needed. There are two exceptions however:
under “Choosing the default editor used by Git” select VS Code not Vim. And in the
section on “Adjusting the name of the initial branch in new repositories” select the option
to use “main” as opposed to “master” as the default branch name. Otherwise the
recommended defaults are fine and can always be tweaked later if needed.

After installing Git
> git config --global user.name "Your Name" 
> git config --global user.email "yourname@email.com" 
> git config --global init.defaultBranch main 

SSH Keys
Unfortunately, there is a good chance that the last command yielded an error if you are a
new developer and do not have SSH keys already configured.
ERROR: Repository not found. 
fatal: Could not read from remote repository. 
Please make sure you have the correct access rights 
and the repository exists. 
This cryptic message means we need to configure SSH keys. This is a one-time thing but a
bit of a hassle to be honest.
SSH is a protocol used to ensure private connections with a remote server. Think of it as
an additional layer of privacy on top of username/password. The process involves
generating unique SSH keys and storing them on your computer so only GitHub can
access them.
First, check whether you have existing SSH keys. Github has a guide to this that works for
Mac, Windows, and Linux. If you don’t have existing public and private keys, you’ll need
to generate them. GitHub, again, has a guide on doing this.
Once complete you should be able to execute the  git push -u origin main  command
successfully!
