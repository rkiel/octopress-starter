Get ready to clone some repositories

    mkdir -p ~/GitHub/imathis
    mkdir -p ~/GitHub/rkiel
    mkdir -p ~/GitHub/yournamehere

clone the Octopress repository

    cd ~/GitHub/imathis
    git clone git://github.com/imathis/octopress.git octopress

clone the octopress-starter repository

    cd ~/GitHub/rkiel
    git clone git://github.com/rkiel/octopress-starter.git

start with a fresh copy of Octopress

    cd ~/GitHub/yournamehere
    cp -r ~/GitHub/imathis/octopress mynewblog

copy the Vagrant files

    cd ~/GitHub/yournamehere/mynewblog
    cp ~/GitHub/rkiel/octopress-starter/Vagrantfile .
    cp -r ~/GitHub/rkiel/octopress-starter/provision provision

make it your own repository

    cd ~/GitHub/yournamehere/mynewblog
    rm -rf .git
    git init
    git add .
    git commit -m "Initial commit"

boot your machine

    vagrant up

login to your machine

    vagrant ssh

add the Heroku toolbelt to your path

    echo 'PATH="/usr/local/heroku/bin:$PATH"' >> ~/.profile
    . .profile

