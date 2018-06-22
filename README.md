# Update command scripts

Want to update your computer software? The update command is for you.

When you run `update` the command will run many software updates and upgrades:

  * Linux: Ubuntu `apt`, RedHat `yum`, Arch `yay`, Fedora `dnf`, etc.
  * macOS: `softwareupdate`, Homebrew `brew`, Mac App Store `mas`, etc.
  * tooling: Node `npm`, Python `pip`, Rust `cargo`, Ruby `gem`, Atom `apm`, etc.
  * source code management: `git pull`, `hg pull`, etc.
  * any of your own custom scripts, before and after everything else.


## Install

Clone the rep:

    $ git clone https://github.com/UpdateCommand/update.git

Add the commands to your path as you like:

    $ export PATH="$PATH:~/update/bin"

Run the script:

    $ update


## Configuration

Create a config directory:

    $ mkdir -p ~/.config/updatecommand

The config home is set by XDG_CONFIG_HOME.

For intermediate users:

  * You may freely add or remove any of the scripts.

  * You may freely edit any of the scripts to match your security preferences.


### Run your own scripts first and last

Do you want to add your own scripts that run first, before all the updates? 

Create this directory and put your scripts in it:

    $ mkdir -p ~/.config/updatecommand/bin/first

Do you want to add your own scripts that run last, after all the updates?

Create this directory and put your scripts in it:

    $ mkdir -p ~/.config/updatecommand/bin/last

For advanced users:

  * The program runs all user-executable files, and skips all non-user-executable files.

  * You can use as many files and subdirectories as you like.


## What's included

This project has Unix update scripts for many tools,
systems, package managers, language modules, et. al.

 * `update`: run all the udpate scripts.
 * `update-apm`: update Atom Package Manager - for the GitHub Atom editor.
 * `update-apt`: update apt-get - for Debian, Ubuntu, etc.
 * `update-brew`: update Homebrew packages - for macOS.
 * `update-brewfile`: update brew packages for macOS by using a Brewfile
 * `update-brew-cask`: update Homebrew Cask packages - for macOS apps.
 * `update-cabal`: update Haskell Cabal pacakages.
 * `update-cargo`: update Rust cargo package manager.
 * `update-cargo-toml`: update Rust cargo package manager Cargo.toml file.
 * `update-carthage`: udpate Xcode Carthage pacakges - for macOS.
 * `update-dnf`: update DNF - for Fedora Linux.
 * `update-hg-pull`: update mercurial repositories.
 * `update-gem`: update Ruby gems.
 * `update-git-pull`: update git repositories.
 * `update-gemfile`: update gem packages for Ruby by using a Gemfile.
 * `update-mas`: update mas packages by using the Mac App Store.
 * `update-motion`: update Ruby Motion - needs a valid paid license.
 * `update-npm`: update Node Package Manager.
 * `update-macos`: update the macOS Mac operating system - large downloads.
 * `update-pacman`: update pacman - for Arch Linux.
 * `update-pip`: update Python PIP.
 * `update-pod`: update Cocoapods for macOS
 * `update-podfile`: update Cocoapods packages for macOS by using a Podfile
 * `update-repos`: update Git repositories - customize this for your system.
 * `update-rustup`: update Rust programming language tooling.
 * `update-swift`: update macOS Swift language - this merely prints advice.
 * `update-ubuntu-release`: update Ubuntu release - for major Linux system upgrades.
 * `update-yay`: update Yay package manager - for Arch Linux

We welcome additions to these scripts.


## To run daily

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @daily /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab


## Configuration files

This tool will also use any of these configuration files:

    ~/.config/Brewfile/Brewfile
    ~/.config/Gemfile/Gemfile
    ~/.config/Podfile/Podfile

The config directory uses the `XDG_CONFIG_HOME` environment variable, which is a POSIX standard environment variable. The default is `$HOME/.config`.


## Tracking

  * Package: UpdateCommand
  * Version: 5.1.0
  * Created: 2005-07-05
  * Updated: 2018-06-22
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
