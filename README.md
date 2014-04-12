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

make it your own repository

    cd ~/GitHub/yournamehere/mynewblog
    rm -rf .git
    git init
    git add .
    git commit -m "Initial commit"
