# Notes on The Odin Project Installfest

This is a test run through The Odin Projects install fest located at <https://www.theodinproject.com/courses/web-development-101/lessons/installations>.

## System

* Processor: Intel(R) Core(TM) i7-7700HQ CPU @ 2.80GHz, 2801 Mhz, 4 Core(s), 8 Logical Processor(s)
* RAM: 16gb 2400MHz DDR4
* HDD: 512GB SSD
* OS: Windows 10

## Installation Procedure

* Download Oracle VM Virtual Box from <https://www.virtualbox.org/> (5.2.12 64-bit)
* Download Ubuntu 16.04 LTS from <https://www.ubuntu.com/download/alternative-downloads>
* Configured VM Virtual Box with 8gb RAM and 10GB HDD
* Configured Ubuntu to use ~8GB HDD for root and ~2gb for swap
* Installed with complete updates to 2018-06-23
* Took system snapshot after updating and before beginning installfest

## Installfest

I decided to take a few approaches to the installfest. The first installation I would move quickly, installing and taking notes as I went but capturing no terminal logs.

I would like to say this was a thought out process but the truth is I started the first round of the installfest without remembering to capture a terminal log.

I would fix errors as they arose and keep track of which areas I had the most difficulty with. Then I would roll back to the clean installation and run through the installfest a second time, capturing all logs and work around as I install. Finally, I would create my own installfest, using what I had learned from the previous attempts, and write out a thorough plan on how to complete the installfest with no errors.

The numbered steps below will be the same steps as posted in the current installfest.

### First Run

1. Install packaged software and libraries. Worked as intended.

   * Found this strange as this was the step most people were having issues with. I had no issues installing any of the packages, no error messages, one message for confirmation of using more disk space. The only thing I can guess is I updated Ubuntu as I installed the OS and the installfest copy / paste skipped over files I had a newer version of. Also, this section would be a good time to remind people that paste in Linux is Ctrl-Shift-V

2. Install Git. Worked as intended.

   * Nothing was installed or updated with this one, probably can be removed.

3. RVM Installation.
   1. Install RVM. Did not change terminal settings as recommended as not using the versions mentioned.

       * First snag. The provided RVM installation does not work. Neither does the suggested step in the installfest. In the terminal there are two options of how to proceed: The first being the suggested step in the installfest. The second being to run the command `command curl -sSL https://rvm.io/mpapis.asc | gpg2 -- import -` which will end up working. However rvm.io suggests using the command `gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB` which is different than any method listed so far. I will try running that on a future attempt.

   2. Configure your shell / verify.

      * Did not return the expected `rvm is a function` instead returned the route to rvm. `rvm -v` also returned something different than expected, but close enough that most would be able to identify the change.

4. Install Ruby

   * It turns out running the terminal in shell mode is absolutely necessary for installing Ruby. Even though the steps for doing this are explained in Step 3 it's not stated as necessary for Ubuntu 16.04 LTS. Recommend either explicitly stating it or maybe there is another terminal we can install first?

5. Install Rails. Worked as intended.

6. Install Atom

   * The instructions in the installfest are basically "Go to the atom website and find out how to install it." That ends up being:

   ```linux
   curl -sL https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
   sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
   sudo apt-get update
   sudo apt-get install atom
   ```

   I would suggest a section on editing programs, listing a few of the easy ones (Atom, Sublime, Notepad++ Visual Studios Code) with the explanation that it's time to learn how to read docs and find the best way to install their editor with the terminal.

7. Configure Git. Worked as intended.

8. Create an SSH key. Worked as intended.

9. Create Heroku Account

   * Since we're trying to avoid snap we should make it apparent that they should not follow the first instructions seen on the page but, instead, use `curl https://cli-assets.heroku.com/install.sh | sh` to install Heroku CLI. Other than that, everything else seems to work as intended.

10. Configure GitHub

    * In the installfest this is listed as an optional step. I know it isn't listed as such in tOP but maybe an explicit instruction that now is a good time to set it up since you have a freshly made SSH key and you remember how to use it?

11. The Heroku App.

    * When pushing the app to Heroku it becomes necessary to update rake with `gem install rake -v '12.3.1'`. There are also several warnings about the bundler being out of date. I suggest the entire section of installing RVM, ruby and Ruby on Rails needs to be re-written. Most of the issues that have ocurred have stemmed from the installation of RVM, or versioning issues with Ruby or Ruby on Rails and the bundles therein.

12. Get a sticker.

    * There are no stickers. This is a critical issue that must be fixed.

### Second Run

VM has been rolled back to snapshot and tested with `ruby -v` which has shown no versions of ruby installed. I have started a log file with `script installfest.txt.` and will add the full text file to the repo upon completion. For this run I will continue to use the commands provided with the installfest EXCEPT the the first massive install library:

```linux
sudo apt-get install autoconf automake bison build-essential curl git-core libapr1 libaprutil1 libc6-dev libltdl-dev libreadline6 libreadline6-dev libsqlite3-0 libsqlite3-dev libssl-dev libtool libxml2-dev libxslt-dev libxslt1-dev libyaml-dev ncurses-dev nodejs openssl sqlite3 zlib1g zlib1g-dev
```

Missing dependencies will be noted and, if necessary, added before continuing.

1. Install packaged software and libraries. Skipped.

2. Install Git. Worked as intended.

    * This time Git actually downloaded and installed something. It appears one of the packages in Step 1 also contains Git?

3. RVM Installation

    1. Install RVM.

        * Curl is not installed. After running `sudo apt install curl` attempted again and failed, using both the installfest recommended method AND rvm.io method. However <https://rvm.io/rvm/install> lists a dedicated Ubuntu package at <https://github.com/rvm/ubuntu_rvm>. Following the instructions there:
        ```linux
        sudo apt-add-repository -y ppa:rael-gc/rvm
        sudo apt-get update
        sudo apt-get install rvm
        ```
         I was able to successfully install RVM. The installation of software-properties-common was not necessary. `rvm -v` returned version 1.29.3

4. Install Ruby

    * At this point I encountered a strange error. Although my preferences were already set to run command as a login shell I could not use `rvm use 2.3`. Instead, I had to `bash --login` to continue at which point everything continued as normal.

5. Install Rails. Worked as intended.

6. Install Atom. Worked as intended (Used truncated installation mentioned above).

7. Configure Git. Worked as intended.

8. Create an SSH key. Worked as intended.

9. Create a Heroku account. Worked as intended (Using the `curl https://cli-assets.heroku.com/install.sh | sh` method).

10. Configure GitHub. Worked as intended.

11. The Heroku App

    * Oh ho ho! We may have finally found something that the packaged libraries supplied to us and I did not have installed! There is no javascript runtime installed at this point! `Rails server` comes back with the "No javascript runtime" error. Running `sudo apt-get install nodejs` fixes the issue.

    * Everything in the heroku installation works fine until the push to heroku occurs. At this point sqlite3 is bundled with the install which is not compatible with Heroku. As we have not installed postgresql at this point I believe that rails falls back to sqlite3 which is incompatible with heroku. Sadly, after a successful `sudo apt-get install postgresql` rails would not generate a scaffold for me. I attempted to remove the bin file and regenerate a new one but I believe that postgresql needs to be installed before working with rails the first time.

12. Get a sticker

    * After this failure I do not believe I deserve a sticker which is just as well as no sticker will be provided. Still a critical issue that has not been fixed.

#### Final thoughts on second run through

I believe that the process of installfest can be drastically reduced and made clearer. Considering that I finished this entire installation in less than an hour (Whereas my previous times had ranged as high as six hours and as low as two) I am excited to try again using the methods I've listed between these two installs. So excited, in fact, that I completely destroyed my log files in my haste to start over and try again.