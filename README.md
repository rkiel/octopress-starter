Get ready to clone some repositories

    mkdir -p ~/GitHub/imathis
    mkdir -p ~/GitHub/rkiel
    mkdir -p ~/GitHub/YOUR-GITHUB-NAME

clone the Octopress repository [first time only]

    cd ~/GitHub/imathis
    git clone git://github.com/imathis/octopress.git octopress

update the Octopress repository

    cd ~/GitHub/imathis/octopress
    git pull

clone the octopress-starter repository [first time only]

    cd ~/GitHub/rkiel
    git clone git://github.com/rkiel/octopress-starter.git

update the octopress-starter repository

    cd ~/GitHub/rkiel/octopress-starter
    git pull

start with a fresh copy of Octopress

    cd ~/GitHub/YOUR-GITHUB-NAME

    cp -r ~/GitHub/imathis/octopress YOUR-BLOG-NAME

copy the Vagrant files

    cd ~/GitHub/YOUR-GITHUB-NAME/YOUR-BLOG-NAME

    cp ~/GitHub/rkiel/octopress-starter/Vagrantfile .
    cp -r ~/GitHub/rkiel/octopress-starter/provision provision
    echo '.vagrant' >> .gitignore

remove the public from .gitignore

    sed -i .bak -e "s/public//" .gitignore

make it your own repository

    cd ~/GitHub/YOUR-GITHUB-NAME/YOUR-BLOG-NAME

    rm -rf .git
    git init
    git add .
    git commit -m "Initial commit"

boot your machine

    vagrant up

login to your machine

    vagrant ssh

    cd /vagrant

install the necessary gems

    bundle install

install Octopress

    rake install

generate your blog

    rake generate

start the blog preview server

    rake preview

hit the blog

    http://192.168.33.10:4000

commit your changes

    git add  public sass source
    git commit -m "Initialize blog"

generate your SSH credentials

    ssh-keygen -b 2048 -t rsa

add your SSH credentials to Heroku

    heroku keys:add ~/.ssh/id_rsa.pub

create a new app on Heroku

    heroku apps:create YOUR-BLOG-NAME

deploy your blog to Heroku

    git push heroku master
