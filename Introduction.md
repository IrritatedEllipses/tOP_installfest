# Introduction

The first step to building anything is having your tools layed out for you. For us that means setting up a development environment in which our code can be created.

Many development courses rely on on-line code editors or sandboxes which give you the tools and dependencies you need at that moment to accomplish the task at hand but nothing else. While you will use some of these sandboxes throughout the early stages of The Odin Project, the best way to set yourself up for success is to operate in a real development environment. We won't lie to you: installing packages, editors, and even entire operating systems can be frustrating at times. However having the experience of setting up a development environment and what is actually needed to run the code you'll write is an invaluable real-world skill you'll carry with you the rest of your career.

## What we are doing

In the following sections we'll be going over the necessary steps for your environment. We will be:

* Installing or configuring the OS of your choice to install the necessary languages.
* Configuring your CLI (Command Line Interface) to facilitate installation and management of development tools.
* Getting Git up and running on your machine.
* Installing NodeJS, a JavaScript runtime environment and package manager.
* Installing RBEnv (A package that helps manage Ruby installations and Gems on your machine), Ruby on Rails, and Ruby itself.
* Selecting and installing a text editor in which you'll code.
* Creating an SSH key, a personal "password" that will identify you to GitHub, Heroku, and many other sites you'll be using.
* And finally, Creating a very basic sampe ruby application and deploying it to Heroku to make sure it all works.

It may seem like a lot of steps but we'll get through it as painlessly as possible together! And, if anything goes wrong, always remember the three rules of problem solving in development:

* Read and try to understand the error message.
* Google, Google, Google.
* Never be afraid to ask for help!

## Options on supported OS'

The first thing we need to decide is what operating system you'll be using to develop on. We've focused on the three that are most prevalent: Linux (Specifically the Ubuntu flavour), MacOS, and Windows. 

### Woah, woah, woah. I like my OS just fine the way it is

That's just fine! We're not asking you to get rid of what you're comfortable with using on a daily basis. You've probably learned a lot of tips and tricks for your favourite OS and don't want to lose everything you have on your computer. But most OS' are developed with non-technical folks in mind and hide or make it difficult for a lot of the languages and frameworks we'll be using to be properly installed without a lot of modification. If they can even be installed at all. Having to work around these difficulties is what causes a lot of new developers to give up before they've even started their journey to Full Stack Nirvana. Modifying or dual booting an OS to work with the tools you'll need will make it much easier to start as a beginner, can help create a distraction free environment, and will look really good on a resume. Take a deep breath and just look at your options.

### Linux

Linux is a free, open source family of operating systems and has the largest install base of all general purpose operating systems. Because of this, most development tools are written to work with the linux kernel first and then ported over to other operating systems with varying degrees of success. Your tools will also most likely be updated more often, have more information available for troubleshooting, and just plain run better with linux. We'll be focusing on the Ubuntu flavour of linux, one of the most popular and user friendly versions available. While some developers choose to change their operating system over to linux entirely (and you can too!) we realize that's not an option available to all. Luckily, linux makes it easy to run with either Windows or MacOS in two different ways:

* Dual-Booting (Running linux "side by side" with your preferred OS).
* Virtual Machines (Running linux "On top" of your preferred OS).

Dual-booting is by far the preferred method for installation. It can be as easy as inserting a USB with the linux installer on it and letting it do it's work while still preserving your preferred OS in place. The benefits of dual-booting cannot be understated: You'll be allowing linux to access the full capabilities of your hardware, have a clean and distraction free environment to do your work in, and be learning the platform that the majority of senior developers and servers in the world use. The Ubuntu flavour of linux is meant to be as user friendly as any Windows or MacOS version with an infinite level of customization just below the surface. And with dual-booting you'll be able to restart the computer to get back to your primary OS at a moments notice. The downside is there is a small, although extremely avoidable, chance of causing issues with the current installation of your preferred OS. Never fear, many people have taken this route before and by carefully following instructions you can avoid causing any problems at all. 

Virtual Machines (VM or VMs), on the other hand, are computers built with software instead of physical components. Through a program like VMWare by Oracle you can create a functioning copy of an existing operating system such as linux. A VM allows you to access the linux OS while still having Windows or MacOS running in the background. You'll computer will treat the VM like any other piece of software, something you load up when needed and close when done and any changes you make to the OS will only effect the program and not your entire OS. Everything you already have on your desktop will be completely accessible at all times, though not able to interact with linux itself (including moving files from your primary OS to your VM without some major work). But there are some drawbacks: The VM will not have complete access to your hardware and can be slow and on some older systems, downright unresponsive at time. Running a VM also uses a lot of your systems resources, making your primary OS slower while the VM is running. And having access to your desktop at all times can lead to unnecessary distractions (Like the three times I checked my desktop notifications while writing this paragraph).

### Mac

If you're not comfortable with the idea of learning a new operating system, or have some experience dealing with the terminal and homebrew, MacOS can function well with most of the tools and languages we'll be using with a little work. MacOS is built upon an architecture quite similar to linux and, though not binary compatible, most languages and packages are ported to the OS with ease. With a few modifications and a little program provided by Apple called XCode you can be up and running with your education in no time! 

However there are a few caveats to using MacOS. You'll always be on your home desktop and all the distractions and problems that can create. While you (and should) create a separate log-in with a clean desktop for all your dev needs, the allure of iMessage can be too strong for some people. Also, while the terminal used by MacOS is similar to the one used in linux it is not exactly the same. A lot of documentation is written with the assumption that you'll be using a linux based system and finding the work arounds for the Mac terminal can be tricky at times. 

### Windows 10 with Linux sub shell

You're probably familiar with Windows for one reason or another and, for many people, it is their OS of choice. It is easy to use, comes installed on most pre-built computers, and many programmed specifically with Windows in mind. Most of us will already be familiar with the Windows interface and not need to adapt to anything new (For good or ill). Unfortunately some languages are not natively made to run on Windows and take a rather large amount of work to get running correctly, if they can be made to run at all. 

Lately a lot of progress has been made to make Windows a more developer friendly atmosphere and, while no where near perfect yet, a linux subsystem is now available in any Windows 10 installation that is running update 16215 or later. However this Windows Subsystem for Linux (WSL) is still in it's infancy. Furthermore, there is a great difficulty in installing a lot of the packages necessary to complete The Odin Project such as Ruby, Ruby on Rails, and even Git. If you use Windows you will have to be vigilant on updates and keep an eye out for any changes that could improve your experience. Most documentation that relies on Command Line Interface (CLI) will not be written with a Windows OS in mind, even one running WSL. This can cause large issues when you're trying to debug or troubleshoot a problem. You should only use Windows if you do not have the ability to dual boot or download VM software.

It can, however, be done if you choose to do so.

### Online editors (Repl.it, CodeBin, JSFiddle, etc...)

There are a variety of online code sandboxes that can be quite handy when you're away from your main system or prototyping some code before committing it. Sites such as:

* Repl.it
* Codepen.io
* JSFiddle.net

Can be used to complete a small exercise or help jot out a concept you might not understand. Though not to be used for any large scale or permanent projects these sites can be used as a tool of their own. If you are just curious about learning to code these sites can be used in the very short term before you're ready to commit to installing anything to your computer. 

### Okay, so which OS should I REALLY use

You should use linux or MacOS. While it is possible to make Windows play nice the bottom line is that a lot of languages and packages, especially Ruby, was made with Unix based operating systems in mind which both linux and MacOS are built from. Considering the frustration required to use Windows as your primary operating system throughout The Odin Project and the ease of dual booting linux or running it in a VM there is almost no reason to choose using Windows over the other choices offered. 

But if you are unable to use anything but Windows for some reason that should not be a barrier to learning how to code. It may be a little more frustrating but being frustrated is better than not learning anything at all.

As a very last resort you can use a variety of online code sandboxes to complete some of the exercises in The Odin Project, though it will not be anywhere near as functional as using an OS. 







