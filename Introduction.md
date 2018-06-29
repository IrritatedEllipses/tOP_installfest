Options on supported OS’s (and advantages/disadvantages of each)
linux (overview and dual-boot options)
mac
windows 10 w/linux subshell
Virtural Machine
Things like Repl.it, Codepen, jsbin etc.
for people not comfortable installing things right away
messing around with code examples
Options for the installs


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
* Creating an SSH key, a personal "password" that will identify you to GitHub, Heroku, and many other sites you'll need.
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

Linux is a free, open source family of operating systems and has the largest install base of all general purpose operating systems. Because of this most development tools are written to work with the linux kernel first and then ported over to other operating systems with varying degrees of success. Your tools will also most likely be updated more often, have more information available for troubleshooting, and just plain run better with linux. We'll be focusing on the Ubuntu flavour of linux, one of the most popular and user friendly versions available. While some developers choose to change their operating system over to linux entirely (and you can too!) we realize that's not an option available to all. Luckily, linux makes it easy to run play with with other OS' in two different ways:

* Dual-Booting (Running linux "side by side" with your preferred OS).
* Virtual Machines (Running linux "On top" of your preferred OS).

Dual-booting is by far the preferred method for installation. It can be as easy as inserting a USB with the linux installer on it and letting it do it's work while still preserving your preferred OS in place. The benefits of dual-booting cannot be understated. You'll be allowing linux to access the full capabilities of your hardware, have a clean and distraction free environment to do your work in, and be learning the platform that the majority of senior developers and servers in the world use. The Ubuntu flavour of linux is meant to be as user friendly as any Windows or MacOS version with an infinite level of customization just below the surface. And, at a moments notice, be able to restart the computer in an instant to get back to your primary OS. The downside is there is a small, although extremely avoidable, chance of causing issues with the current installation of your preferred OS. Never fear, many people have taken this route before and by carefully following the instructions you can avoid causing any problems at all. 

Virtual Machines (VM or VMs), on the other hand, are computers built with software instead of physical components. Through a program like VMWare by Oracle you can create a INSERT DESCRIPTION HERE. A VM allows you to access the linux OS while still having Windows or MacOS running in the background. You'll computer will treat the VM like any other piece of software, something you load up when needed and close when done while the programs you install in Linux will be walled off from your primary OS. Everything you already have on your desktop will be completely accessible at all times though not able to interact with what's in Linux. But there are some drawbacks: The VM will not have complete access to your hardware and can be slow and, on some older systems, downright unresponsive at time. Running a VM also uses a lot of your systems resources, making your primary OS slower while the VM is running. And having access to your desktop at all times can lead to unnecessary distractions (Like the three times I checked my desktop notifications while writing this paragraph).

### Mac

YOU GUYS I DON'T KNOW ANYTHING ABOUT MAC SO SOMEONES GONNA HAVE TO FILL THIS OUT KTHX

### Windows 10 with Linux sub shell









