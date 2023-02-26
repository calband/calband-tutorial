# Computer Assistant Onboarding

## Introduction

Thank you for your interest in joining the Cal Band Computer Committee! During your time as a CA or on HACK, you will help the band function faster and better on Members Only, our Recruit site, or on CalChart! You will learn software engineering skills by collaborating on GitHub, setting up a developer environment, and designing and testing features that are used by the 200+ members of the Cal Band!

If you are reading this, you already have a GitHub account and have been added to our organization. Hooray! Next, please join the [Google Drive](https://drive.google.com/drive/folders/1Q_Z76nEyfy-o6hsey9qxUq-1ix5LUQGk?usp=sharing) if you haven't already. This will contain our meeting notes/other CompComm resources for projects. 

You will be diving into a large codebase while learning new technologies. Having previous experience with large projects will be very helpful.

In this tutorial, you will learn the basics of how to use Github to collaborate and how to create a [simple Django web application](https://youtu.be/ZjOUc7rKtPQ).

## Git for Beginners
Do this step first if you have never used git before!
### Mac Users

1) Install homebrew by going to your terminal and entering the following: 

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

You may be prompted to enter your computer password. To check if brew is working after installation, enter this into your terminal:
```
brew doctor
```

2) Install git by entering this into your terminal: 
```
brew install git
```
Verify that git is working by entering this:
```
git --version
```
### Windows Users

Follow the "Installing Git" instructions [here.](https://fa22.datastructur.es/materials/lab/lab01/windows.html#b-install-git)

## Git set up

We strongly recommend that you set up a SSH key that's paired up with Github. Follow this [tutorial](https://help.github.com/articles/connecting-to-github-with-ssh/).

Open up your terminal and `cd` into a folder that you want to clone this tutorial folder in.

```
git clone git@github.com:calband/calband-tutorial.git (or use the https link: https://github.com/calband/calband-tutorial.git)
```

Next, we'll create a new branch for you to make changes on.

```
git checkout -b ["enter your name here!!! this is the name of your branch"]
```

## Virtual Machine Set Up

Finally, we'll set up your Virtual Machine.

1. Install VirtualBox
2. Install Vagrant

Make sure that your terminal is in the calband-tutorial folder, and run `vagrant up`. This will create the VM and install everything it needs to get running. It is common to run into trouble at this step, particularly for Windows users. Please ask the Computer Coordinators with help in setting up your computer. You may need to run `vagrant reload` or `vagrant destroy` so you can bring up the VM again. 

For the rest of the tutorial, make sure that you're SSH'd into your VM and are using the proper commands. 
**If you are having issues, feel free to skip these steps for now and continue to complete the Django tutorial below.**

1. Run `vagrant ssh` to SSH into your VM
2. Run `cd /vagrant` to get into the mounted folder (the calband-tutorial folder syncs up with this folder on your VM)
3. When the Django tutorial tells you to use `python`, make sure to use `python3.6`. Example: `python3.6 manage.py runserver`.

## Your Task

You will complete the ["Writing your first Django app" tutorial](https://docs.djangoproject.com/en/4.1/intro/tutorial01/). Do not worry about "Database setup" in part 2. Since we use PostgreSQL, after you run the `django-admin startproject mysite` command in part 1, go into `mysite/settings.py` and change the `DATABASES` variable to the following:

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'members_only_db',
        'USER': 'members_only_user',
        'PASSWORD': 'calbandgreat',
        'HOST': '127.0.0.1'
    },
}
```

If you are having trouble with getting your mind around setting up Django, look to [this](https://simpleisbetterthancomplex.com/series/2017/09/04/a-complete-beginners-guide-to-django-part-1.html#starting-a-new-project) guide. If you still aren't sure about something ask the Computer Manager, HACK, or someone on Comp Comm and they'd be glad to help!

When you finish, you will make a pull request to show off your progress! In our workflow, we use pull requests to help us review changes made before making a changes to our master branch.

```
git status
git add .
git commit -m "Finished tutorial! Cal Band Great! Wow"
git push origin [the name of your branch]
```

This process creates a new branch. It also stores your changes into a commit. Finally, it pushes the commit that is stored on your computer to Github.

Open up the Github repository. You should see a yellow box with your branch. Smash that mf pull request button!!! Submit a pull request!!! You did it!!! WoooOooOOOoOoOOOooOOOOOOOOOO!! You should see that the Computer Coordinators have created pull requests as well!

## Congratulations

[Congratulations!!!](https://youtu.be/1Bix44C1EzY)

Just by completing this tutorial, you've accomplished so much!!! You now have the basic knowledge to contribute to the Computer Committee! [Yee haw](https://youtu.be/M0Ncawy2LJc)!

##

## Optional tutorials

These outside tutorials are very helpful in understanding other technologies that you will use. Although you can learn these while working on issues, these tutorials will better prepare you. In particular, you should learn about HTML, SCSS, jQuery, and git. You can apply what you learned in those tutorials in your PR!

- [Brandon Chinn's (Computer Coordinator 2016) guide to everything comp comm related](https://github.com/calband/compcomm-info)
- [Web Design Decal CSS Cheat Sheet](https://docs.google.com/document/d/1P8W1Fl__4fwui-Sac5UjauTvyj-NLhcgLk_5el82_5A/edit?usp=sharing) You have to use your berkeley account to access this.
- [Codecademy HTML + CSS](https://www.codecademy.com/en/tracks/web)
- [Javascript Fundamentals](https://javascript.info/first-steps)
- [try.jquery.com](http://try.jquery.com/levels/1/challenges/1)
- [What is Sass?](https://www.creativebloq.com/web-design/what-is-sass-111517618)
- [try.github.io](https://try.github.io/levels/1/challenges/1)
