# docker_installs
This script will help install any, or all, of Docker-CE, Docker-Compose, NGinX Proxy Manager, and Portainer-CE.

## Reason for Making this Script
I got tired of running individual commands all the time, so I created some scripts to make this very easy. 

## Using this script

1. Clone the repo
`git clone https://gitlab.com/bmcgonag/docker_installs.git`

, or copy / paste the code from the `install_docker_nproxyman.sh` file into a file on your server. 

`nano docker-install.sh`

to open a text editor in the terminal, then use CTRL + Shift + V to paste into it.

Save with CTRL + O, then Enter to confirm, and exit the nano editor with CTRL + X.

2. Change the permissions of the .sh file to make it executable with.

`chmod +x docker-install.sh`

3. Run the installer with

`./docker-install.sh`

## Prompts from the script:
First, you'll be prompted to select the number for your OS / Distro.  Currently I support RaspbianOS (latest), CentOS 7 and 8, Debian 10 and 11, Ubuntu 18.04, 20.04, 22.04, 23.05, Arch Linux, and Open Suse (tested on Leap 15.4). 

Next, you'll be asked to answer "y" to any of the four software packages you'd like to install. 
- Docker-CE (you'll need this for the others to work)
- Docker-Compose (you'll need this for any of the applications to start properly)
- NGinx Proxy Manager
- Navidrome (music player)
- Remotely (Remote Desktop Support Tool)
- Guacamole (Remote Desktop Protocol in the Browser)
- Portainer-CE
  - if you answer y to Portainer, you'll be asked another question

Do you want 
  1. full Portainer-CE with the web UI, or 
  2. just Portainer-agent (which you connect to another full portainer instance). 

Make that selection, and the install will continue.

Answering "n" to any of them will cause them to be skipped.

### NOTE
* You must have Docker-CE (or some version of Docker) installed in order to run any of the other three packages.
* You must have Docker-Compose installed in order to run NGinX Proxy Manager, Portainer-CE, or any of the apps offered with this script.

Before prompting to install Docker or Docker-Compose, I do try to see if you already have them installed, and I skip the prompt if you do (or I try to anyway).

## Recent changes
- Added option for Raspbian install with Arm64 Chips.
- Added Remotely as an application option
- Added Guacamole as an application option

## Future Work
- [X] Make it work for Raspberry Pi
- [X] Make it work for Arch
- [X] Make it work for OpenSuse
- [X] Maybe add a few other default containers to pull down and start running
- [ ] Prompt for Credentials to use in NGinX Proxy Manager db settings vs. using the defaults.
- [X] Set all Conteiners on a single docker network
- [ ] Clean it up and split out functions to other files to make it easier to run / work on.

## Contributing
If you find issues, please let me know. I'm always open to new contributors helping me add Distro support, more software packages, etc.  Just clone the project and make a pull request with any changes you add. 

## Licensing
My script is offered without warranty against defect, and is free for you to use any way / time you want.  You may modify it in any way you see fit.  Please see the individual project pages of the software packages for their licensing.

## Contributors
@binuengoor
