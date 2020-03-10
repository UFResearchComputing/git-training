# UF Research Computing git and gitbub.com training

This training will start with some slides which are in the gh-pages branch and online at <https://ufresearchcomputing.github.io/git-training/#/>

After going over the slides, we'll come back to this.

## Resources

There are many great git and github.com tutorials out there. Here are some that I particularly like and have relied on in developing this training.

Source | Notes
-------|------
[Software Carpentry Version Control with Git](http://swcarpentry.github.io/git-novice/) | This is a popular module in the Software Carpentry curriculum. It is designed to be a 3-hour instructor-lead training module but can be worked through on your own as well.
[GitHub Learning Lab](https://lab.github.com/) | This site has many lessons that use github.com and automation to walk users through hands-on exercises to learn aspects of git and github.com using the tools.
[try.github.io/](https://try.github.io/) | More github tutorials


## Setup
The [git_setup.md](git_setup.md) page has some basic git and github configuration information.

## Hands-on exercise

This exercise is adapted from the Software Carpentry [Version Control with Git](http://swcarpentry.github.io/git-novice/) training.

This exercise tells the tail of Wolfman and Dracula who are investigating if it is possible to send a planetary lander to Mars.

![Cartoon of Wolfman and Dracula](images/motivatingexample.png)[Werewolf vs dracula](https://www.deviantart.com/b-maze/art/Werewolf-vs-Dracula-124893530)
by [b-maze](https://www.deviantart.com/b-maze) / [Deviant Art](https://www.deviantart.com/).
[Mars](https://en.wikipedia.org/wiki/File:OSIRIS_Mars_true_color.jpg) by European Space Agency /
[CC-BY-SA 3.0 IGO](https://creativecommons.org/licenses/by/3.0/deed.en).
[Pluto](https://commons.wikimedia.org/wiki/File:PIA19873-Pluto-NewHorizons-FlyingPastImage-20150714-transparent.png) /
Courtesy NASA/JPL-Caltech.
[Mummy](https://commons.wikimedia.org/wiki/File:Mummy_icon_-_Noun_Project_4070.svg)
&copy; Gilad Fried / [The Noun Project](https://thenounproject.com/) /
[CC BY 3.0](https://creativecommons.org/licenses/by/3.0/deed.en).
[Moon](https://commons.wikimedia.org/wiki/File:Lune_ico.png)
&copy; Luc Viatour / [https://lucnix.be](https://lucnix.be/) /
[CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en).

### Creating a Repository

While we can start creating the repository from scratch, I typically find it easier to create the repo online, clone it to the local computer (or cluster), add the content and `push` the changes.

To create a new repo, on github.com, click the +-icon in the top right and select New repository:

![Screenshot of create repo icon](images/git_new_repo.png)

Let's call this repo "planets" and leave the rest of the settings with the defaults and click Create repository:

![Screenshot of the create repo page](images/git_new_repo_details.png)

Note that I have my account setup for SSH keys, so I clicked the "SSH" button circled in red below. If you have not setup SSK keys and two-factor authentication, you can leave the HTTPS button clicked. 

![Screen shot of the info to make a new repo](images/git_new_repo_info.png)

At this point, we have a repository, but there isn't anything in it. GitHub provides a number of options about what we can do from here. For this tutorial, I will use the "…or create a new repository on the command line" instructions.
I will do this in my account on HiPerGator, but you could do it on your computer (use the Terminal on Mac or Git Bash on Windows).

1. Log into HiPerGator: `ssh *gatorlink*@hpg.rc.ufl.edu`
1. Make a directory for this repository: `mkdir planets`
   * It is best if the directory name matches the repository name
1. Change directories into this new folder: `cd planets`
1. Copy the commands in the "…or create a new repository on the command line" box on the github page and then past them into your terminal--**Make sure you are in the `planets` directory**:
   * These commands do a number of things:
      * `echo "# planets" >> README.md` Creates the starts of the README.md document for the repo.
      * `git init` Tells Git that this is a git repository and creates all the infrastructure to treat it as such.
      * `git add README.md` Places the README.md file in the staging area and tells Git to track changes to this file.
      * `git commit -m "first commit"` Commits the changes to the local repo. This records the changes and sets a point in history that can be recovered.
      * `git remote add origin git@github.com:*magitz*/planets.git` This connects the local repo to the one on GitHub that we made to start with. **Note:** My github username is *magitz*, you will need to use your username.
      * `git push -u origin master` This `push`es our changes to GitHub.
         * If you have not setup SSH keys, you will be asked for your github.com username and password.

## Continue on the [Hands-on page 2](Hands-on2.md)


