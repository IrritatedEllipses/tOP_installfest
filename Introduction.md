# Introduction

The first step to building anything is having your tools layed out for you. For us that means setting up a development environment in which our code can be created.

Many development courses use online code editors or "sandboxes" which give you the tools and programs you need at that moment to accomplish the task at hand, but nothing else. While you will use some of these sandboxes throughout the early stages of The Odin Project (They're great for getting started quickly), the best way to set yourself up for success is to operate in a real development environment. We won't lie to you: installing packages, editors, and even entire operating systems can be frustrating at times. However having the experience of setting up a development environment and what is actually needed to run the code you'll write is an invaluable real-world skill you'll carry with you the rest of your career.

## What we are doing

In the following sections we'll be going over the necessary steps for your environment. We will be:

* Installing or configuring the OS (Operating System) of your choice.
* Configuring your CLI (Command Line Interface) to install the necessary development tools.
* Getting Git up and running on your machine.
* Installing all the languages and frameworks you'll need for The Odin Project. These include NodeJS, Ruby, and Ruby on Rails.
* Selecting and installing a text editor.
* Creating an SSH key, a personal "password" that will identify you to GitHub, Heroku, and many other sites you'll be using.
* And finally, Creating a very basic sampe ruby application and deploying it to Heroku to make sure it all works.

It may seem like a lot of steps but we'll get through it as painlessly as possible together! And, if anything goes wrong, always remember the three rules of problem solving in development:

* Read and try to understand the error message.
* Google, Google, Google.
* Never be afraid to ask for help!

## Options on supported OS'

The first thing we need to decide is what operating system you'll be using to develop on. We've focused on the big three: Linux (Ubuntu), MacOS, and Windows. 

### Woah, woah, woah. I like my OS just fine the way it is

That's just fine! We're not asking you to get rid of what you're comfortable with using on a daily basis. You've probably learned a lot of tips and tricks for your favourite OS and don't want to lose everything you have on your computer. But most OS' are developed with non-technical folks in mind and hide or make it difficult for a lot of the languages and frameworks we'll be using to be properly installed without a lot of modification. If they can even be installed at all. Having to work around these difficulties is what causes a lot of new developers to give up before they've even started their journey to Full Stack Nirvana. Modifying or dual booting a computer to work with the tools you'll need will make it much easier to start as a beginner, can help create a distraction free environment, and will look really good on your resume. Take a deep breath and just look at your options.

### Mac

If you're using a Mac you're in great shape.  Most professional developers rely on Macs to code on. By just installing a few programs you will be up and running with your education in no time!

### Linux

Linux is a free operating system that works well with all programming languages. Most development tools are written to work nativly with Linux . Your tools will likely be updated more often, have more information available for troubleshooting, and just plain run better with linux. We'll be focusing on the Ubuntu flavour of linux, one of the most popular and user friendly versions available. While some developers choose to move entirely to linux (and you can too!), we realize that's not an option available to all. Luckily there are two different ways you can use both Windows and Linux:

* Dual-Booting (Running linux "side by side" with Windows).
* Virtual Machines (Running linux "On top" of Windows).

Dual-booting is by far the preferred method for installation. It can be as easy as inserting a USB and clicking a fe buttons. This method will install Linux along side of your Windows OS, so none of your data will be lost. The benefits of dual-booting cannot be understated: You'll be allowing linux to access the full capabilities of your hardware, have a clean and distraction free environment to do your work in, and be learning the platform that the majority of senior developers and servers in the world use. 

The Ubuntu flavour of linux is meant to be as user friendly as any Windows or MacOS version with an infinite level of customization just below the surface. And with dual-booting you'll be able to restart the computer to get back to your primary OS at a moments notice. The only downside, though _very_ small, is the chance of causing issues with your current OS. These issues are very rare and can usually be recovered from. Never fear, many people have taken this route before and by carefully following instructions you can avoid causing any problems at all. This is the prefered way to install Linux.

Virtual Machines (VM or VMs), on the other hand, are computers built with software instead of physical components. Using a free program like Virtualbox by Oracle you can create a functioning "computer" and install Linux. A VM allows you to access the linux OS while still having Windows running in the background. You'll computer will treat the VM like any other piece of software, something you load up when needed and close when you're done. But there are some drawbacks; VMs are not as fast as Dual-booting because your physical computer has to support two Operating Systems. This can make both the VM and Windows very slow.

### Windows 10 with Linux Subsystem

You're probably familiar with Windows for one reason or another; For many people, it is their OS of choice. It is easy to use and comes pre-installed on most computers. Unfortunately some languages are not easily made to run on Windows or take a large amount of work to get running correctly.

Lately a lot of progress has been made to make Windows a more developer friendly atmosphere and while no where near perfect yet, the Linux Subsystem for Windows (WSL) is now available in most any Windows 10 installations. However WSL is still in it's infancy and can be buggy. If you use Windows and run into issues it might be harder to figure out the solution. We don't recommend WSL but it can be used if you have no other options.

### Online editors (Repl.it, CodeBin, JSFiddle, etc...)

There are a variety of online code sandboxes that can be quite handy when you're away from your main system or prototyping some code before committing it. Sites such as:

* Repl.it
* Codepen.io
* JSFiddle.net

Can be used to complete a small exercise or help jot out a concept you might not understand. However, you shouldn't use these sites as your main development environment. These sites can be used in the very short term until you're ready to commit to installing anything to your computer. 

### Okay, so which OS should I REALLY use

You should use Linux or MacOS. 

While it is possible to make Windows play nice the bottom line is that a lot of languages and packages, especially Ruby, were designed with Unix (Linux and macOS) based operating systems in mind. Considering the frustration required to develop in Windows and the ease of dual booting or running a VM, there is almost no reason to choose Windows. 







