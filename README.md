# calband-tutorial: Computer Assistant Onboarding

## Introduction

Thank you for your interest in joining the Cal Band Computer Committee! During your time as a CA or on HACK, you will help the band function faster and better on Members Only, our Recruit site, or on CalChart! You will learn software engineering skills by collaborating on Github, setting up a developer environment, and designing and testing features that are used by the 240+ members of the Cal Band!

It is recommended that CAs and HACK have taken or are taking at least CS61B, so this tutorial won't dive deep into basic coding/git commands. You will be diving into a large codebase while learning new technologies. Having previous experience with large projects will be very helpful.

In this tutorial, you will learn the basics of how to use Github to collaborate and how to create a [simple Django web application](https://youtu.be/Dma8Cq2i0cc?t=41s).

## Set up

First, you should [download](https://www.python.org/) the latest Python distribution. Second, download Django. The easiest way is through [pip](https://pip.pypa.io/en/stable/installing/) or pip3 (whichever one is the Python3 version) below. You can read the actual Django docs if you want.

```
pip install Django
pip3 install Django
```

Open up your terminal and `cd` into a folder that you want to clone this tutorial folder in.

```
git clone git@github.com:calband/calband-tutorial.git (or use the https link: https://github.com/calband/calband-tutorial.git)
cd calband-tutorial
ls
```

This should print out `README.md`

Next, we'll create a new branch for you to make changes on.

```
git checkout -b [enter your name here!!! this is the name of your branch]
```

## Your Task

You will complete the ["Writing your first Django app" tutorial](https://docs.djangoproject.com/en/2.0/intro/tutorial01/). Do not worry about "Database setup" in part 2. You will use SQLite for simplicity.

When you finish, you will make a pull request to show off your progress! In our workflow, we use pull requests to help us review changes made before making a changes to our master branch.

```
git status
git add .
git commit -m "Finished tutorial! Cal Band Great! Wow"
git push origin [the name of your branch]
```

This process creates a new branch. It also stores your changes into a commit. Finally, it pushes the commit that is stored on your computer to Github.

Open up the Github repository. You should see a yellow box with your branch. Smash that mf pull request button!!! Submit a pull request!!! You did it!!! WoooOooOOOoOoOOOooOOOOOOOOOO

## Congratulations

[Congratulations!!!](https://youtu.be/1Bix44C1EzY)

Just by completing this tutorial, you've accomplished so much!!! You now have the basic knowledge to contribute to the computer committee! My [--insert your gender identifier--](https://youtu.be/I04OIfbBrTg)!

## Optional tutorials

These outside tutorials are very helpful in understanding other technologies that you will use. Although you can learn these while working on issues, these tutorials will better prepare you. In particular, you should learn about HTML, SCSS, jQuery, and git. You can apply what you learned in those tutorials in your PR!

- [Brandon Chinn's (Computer Coordinator 2016) guide to everything comp comm related](https://github.com/calband/compcomm-info)
- [Web Design Decal CSS Cheat Sheet](https://docs.google.com/document/d/1P8W1Fl__4fwui-Sac5UjauTvyj-NLhcgLk_5el82_5A/edit?usp=sharing) You have to use your berkeley account to access this.
- [Codecademy HTML + CSS](https://www.codecademy.com/en/tracks/web)
- [Javascript Fundamentals](https://javascript.info/first-steps)
- [try.jquery.com](http://try.jquery.com/levels/1/challenges/1)
- [What is Sass?](https://www.creativebloq.com/web-design/what-is-sass-111517618)
- [try.github.io](https://try.github.io/levels/1/challenges/1)
