DTCH
====

DreamTeam

# Prerequisites:
### Ubuntu 18 iso file
### VirtualBox installed

# Minimal install of Ubuntu in VirtualBox
## open terminal
- sudo ufw enable
- sudo apt-get install gcc
- sudo apt-get install make
# Install guest additions

# Installi python 3.7
- sudo apt update
- sudo apt install software-properties-common
- sudo add-apt-repository ppa:deadsnakes/ppa
- sudo apt install python3.7
- sudo apt-get install git
- snap install atom --classic
- sudo apt-get install python3-pip
- sudo apt-get install vim

# SETUP GITHUB SSH KEY
- ssh-keygen -t rsa -b 4096 -C "email@address"
- eval "$(ssh-agent -s)"
- ssh-add ~/.ssh/id_rsa
- sudo apt-get install xclip
- xclip -sel clip < ~/.ssh/id_rsa.pub
- goto: https://github.com/settings/keys
- create new key and copy clipboard into it.

# Optional nice prompt

## ~/.bash_prompt (contents:)

    parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
    }

    PS1='\[\e]0;\u@\h: \w\a\]\[\e[1;33m\]\u@\h \w \n\[\e[1;36m\] \@ \d\$\[\e[m\] $(parse_git_branch) \n:'

    export PS1

## Add this to .bashrc:
    if [ -f ~/.bash_prompt ]; then
        . ~/.bash_prompt
    fi
