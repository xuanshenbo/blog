---
layout: post
title: "Github Basic Tutorial"
description: ""
category: Tutorial
main-class: 'jekyll'
image: https://lh3.googleusercontent.com/m0M5-Ge6_KpDX_umEFKFzbkJ-KE36hDOhI8B4FjIZK3ff7wHlp1WO9eKRWkSLAz1-Vro7faYDd83IdTc869ESzpiq4d5ECCXI326p1EL5JK3UDlYb1yJaU8utowvcFTl_U6uoZv9NkD1awZ9nCR7PjiPeFV1xxfoZVShIqnQq9xXkrNZOZI1Qh3O_tMt13kF3KBr15dsE-zF10ngaAMilkOEIeJLJXQTfeZmom3ngbSCWFemNDPPd5PwugyRf3OFvEvbHMqOIx3SIlQ2VeYvzpcOIXLAhjc0esiOFlov6u8S6NX9pSTjN0F08mv_uAyHnQx9Oz4S3UtwJfVnmyHA1KZ8ve-A0_msBTjxnp1LP3PCMUiITADFEbSHPNQrTpNp4u9QbSAnWo-V4iGt9dG4vzqDeau8xDcEJhAk67oZV4Nw-GK_1nci1x0OmCAVxjs429sZext_Ynj6Hev2KHOyZN7J1K4EhJNKYFuwBWLkA-5qdgyqBgkBgoptmat4yWSkGgBg8zC1eIPcSoCOqb99Tlrc4xFnHYdlwNhb_nFqR7wd5hjhVF8RQZDvJavli23-JVX6YAPuP5eZK2C3F-8LIewMUCkoaHpuZP0mWy6kOQdyoH2CaOihN3qc7bIHyPq0tV7ypvh2OsuwdSv7FARqoHXW4IBXcsk=w1200-h630-no
tags: [Github]
---
This tutorial is made for SWEN222 project team members, however everyone can use it as a quick tutorial. It only has extremely basic operations.

<!--more-->


1. [Create a Java project in Eclipse](#Create Project)
2. [Initialise your Git configuration for your project](#Initialise Git)
3. [Pull the project](#Pull)
4. [Make changes](#Modify)
5. [Commit and push](#Push)
6. [In the future](#Future)
7. [Some notes](#Notes)

Create a Java project in Eclipse <a id="Create Project"></a>
------

**Note:** For simplicity I use Eclipse here as an example, feel free to use other IDEs or editors.

You should know how to do it I'm not gonna say anything here.

---

Initialise your Git configuration for your project <a id="Initialise Git"></a>
------

Now, go to your ```src``` file under your project and type the following command:

```
% git init
```

Now you should have created a hidden file ```.git/```. This means you have initialised your directory to a git directory.

To view all your files in the current directory type the command ```ls -a```. If you don't have a ```.git/``` file you did something wrong!

Now go ahead and type the following command:

```
% git remote add origin https://github.com/xuanshenbo/Test-Github
```

**Note:** The reason why we init our directory in the ```src``` directory not the project directory is because the project directory contains a bunch of configuration files for IDEs and also bin files. Since we don't want to mess up others' IDEs and we are only interested in the source files in our case, ```src``` would be a better place for us. So make sure all your source code including images are under your ```src``` directory.

---

Pull the project <a id="Pull"></a>
------

I have created a project for us:

<a href="https://github.com/xuanshenbo/Test-Github"> Test-Github</a>

Now under you ```src``` directory, type the following command:

```
% git pull https://github.com/xuanshenbo/Test-Github
```

Now refresh your project in your Eclipse you will see a test package.

---

Make changes <a id="Modify"></a>
------

Feel free to modify the class named after you. Please do not modify others' classes at this stage because we don't want to deal with conflicts. Actually this tutorial will not cover conflicts we will talk about this in our group meeting.

If you are not in our group, feel free to create a class named after yourself.

---

Commit and Push <a id="Push"></a>
------

**NOTE:** Before doing this step, make sure you are one of the collaborators of the project. You need to email me your log-in name so I can add you as a collaborator.

Now type the following command:

```
% git add .
```
where ```.``` means all

And then:

```
% git commit -m "comment message"
```
make sure your comment message is clear and sensible. **IT WILL BE MARKED FOR THE PROJECT!!!**

Then:

```
% git push -u origin master
```

Now it will ask for your username and password, after that you are done!

---

In the future <a id="Future"></a>
------

Since we had done the initilisation part, in the future we will mainly be using the pull and push parts. It is pretty much like the first time only that when you do the ```git push -u origin master``` part, you don't have to type the whole thing, ```git push``` will do.

---

Some notes <a id="Notes"></a>
------

**NOTE:** As mentioned above, our commit comments will be marked, not only that, a nice and clear comment always helps. We don't want to hate ourselves 10 days later when we have to know what we did.

**NOTE:** In general, when we do ```git add``` we simply add ```.``` which stands for all. However you can add a single file if you want.

**NOTE:** For now we do not need many other features these will be enough, in the future when we have to we might explore more.

**NOTE:** Most of the time, before a push, pull the project to make sure your projet is up-to-date. In fact I don't think Git allows you to push without a pull.

**NOTE:** Don't worry if we may have found that we like our previous version more, we can always find our previous versions. So make sure you push frequently!

**NOTE:** Generally you want to do all the operations exactly in the ```src``` directory.
