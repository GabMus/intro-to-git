<!-- $theme: default -->

<!-- $size: 4:3 -->


# git 101

## State of the art source management and version control


<img width="250" src="https://upload.wikimedia.org/wikipedia/commons/e/e0/Git-logo.svg" />

##### by Gabriele Musco

<br /><br />

<font size="4" color="grey">*"Intro to git" is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
You should have received a copy of the license along with this work.
If not, see <http://creativecommons.org/licenses/by-sa/4.0/>.*</font>

---

# What is git?

<img height="200" src="https://git-scm.com/images/branching-illustration@2x.png" />

- (*Free and open source software)*
- Distributed version control system (VCS)
- Collaborative work platform
- **Essential** software development tool

---

# What is a *version control system*?

<img src="./assets/gitflow.svg" />

Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.

---

# Why should I care?

- Revert selected files back to a previous state
- Revert the entire project back to a previous state
- Compare changes over time
- See who last modified something that might be causing a problem, who introduced an issue and when

---

# How git can save your bacon :bacon:

<script src="https://asciinema.org/a/Gexg5CxFjBQqOkzHA80fK29L4.js" id="asciicast-Gexg5CxFjBQqOkzHA80fK29L4" async data-size="medium" data-theme="monokai"></script>

---

# Some history

- Created by Linus Torvalds in 2005 to manage the Linux source code

![](https://i.imgur.com/OtDQT5v.gif)

- Designed to be *fast* and simple to use

---

## Trivia

> The name "git" was given by Linus Torvalds when he wrote the very first version. He described the tool as "the stupid content tracker" and the name as (depending on your way):
> - random three-letter combination that is pronounceable, and not actually used by any common UNIX command. The fact that it is a mispronunciation of "get" may or may not be relevant.
> - stupid. contemptible and despicable. simple. Take your pick from the dictionary of slang.
> - "global information tracker": you're in a good mood, and it actually works for you. Angels sing, and a light suddenly fills the room.
> - "goddamn idiotic truckload of shit": when it breaks

---

# Git is distributed

- Every *clone* of a git repo is exactly identical to the original one
- Allows for many different **workflows**

---

# Some popular workflows

---

# Subversion style
### (don't use this)

![](https://git-scm.com/images/about/workflow-a@2x.png)

---

# Integration Manager
### (aka what you do on GitHub)

![](https://git-scm.com/images/about/workflow-b@2x.png)

---

# Dictator and Lieutenants
### (how it's done with the Linux kernel)

![](https://git-scm.com/images/about/workflow-c@2x.png)

---

# All of this is possible thanks to git's flexibility.

---

# ![](https://dwa5x7aod66zk.cloudfront.net/assets/labtocat-be5eee0434960a8f73e54910df8e87b8a5a3b2d651c0b301670c04a9cc26a70f.png) Lab time!

---

![](https://dwa5x7aod66zk.cloudfront.net/assets/labtocat-be5eee0434960a8f73e54910df8e87b8a5a3b2d651c0b301670c04a9cc26a70f.png)

## Requirements:

- <svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M4,6H20V16H4M20,18A2,2 0 0,0 22,16V6C22,4.89 21.1,4 20,4H4C2.89,4 2,4.89 2,6V16A2,2 0 0,0 4,18H0V20H24V18H20Z" /></svg> A PC
- <svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M20,19V7H4V19H20M20,3A2,2 0 0,1 22,5V19A2,2 0 0,1 20,21H4A2,2 0 0,1 2,19V5C2,3.89 2.9,3 4,3H20M13,17V15H18V17H13M9.58,13L5.57,9H8.4L11.7,12.3C12.09,12.69 12.09,13.33 11.7,13.72L8.42,17H5.59L9.58,13Z" /></svg> A terminal
- <svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M2.6,10.59L8.38,4.8L10.07,6.5C9.83,7.35 10.22,8.28 11,8.73V14.27C10.4,14.61 10,15.26 10,16A2,2 0 0,0 12,18A2,2 0 0,0 14,16C14,15.26 13.6,14.61 13,14.27V9.41L15.07,11.5C15,11.65 15,11.82 15,12A2,2 0 0,0 17,14A2,2 0 0,0 19,12A2,2 0 0,0 17,10C16.82,10 16.65,10 16.5,10.07L13.93,7.5C14.19,6.57 13.71,5.55 12.78,5.16C12.35,5 11.9,4.96 11.5,5.07L9.8,3.38L10.59,2.6C11.37,1.81 12.63,1.81 13.41,2.6L21.4,10.59C22.19,11.37 22.19,12.63 21.4,13.41L13.41,21.4C12.63,22.19 11.37,22.19 10.59,21.4L2.6,13.41C1.81,12.63 1.81,11.37 2.6,10.59Z" /></svg> Git installed
- <svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z" /></svg> A GitHub account (<https://github.com/join>)
- <svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#000000" d="M1.5,4V5.5C1.5,9.65 3.71,13.28 7,15.3V20H22V18C22,15.34 16.67,14 14,14C14,14 13.83,14 13.75,14C9,14 5,10 5,5.5V4M14,4A4,4 0 0,0 10,8A4,4 0 0,0 14,12A4,4 0 0,0 18,8A4,4 0 0,0 14,4Z" /></svg> A friend!

---

# Form groups of two

<audio controls>
	<source src="./assets/sounds/quake_prepare_to_fight.opus" type="audio/ogg" />
</audio>

---

# Installing git

### Debian/Ubuntu `sudo apt-get install git`

### Fedora `sudo dnf install git`

### Gentoo `sudo emerge --ask --verbose dev-vcs/git`

### Arch Linux/Antergos/Manjaro `sudo pacman -S git`

### openSUSE `sudo zypper install git`

<br /><br />

###### Windows

<font size="4">If you really have to use it, install the WSL and git on top of it. Alternatively use a VM.</font>

---

