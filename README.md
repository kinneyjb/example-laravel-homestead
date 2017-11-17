Install php71

    $ brew update
    $ brew upgrade
    $ brew tap homebrew/dupes
    $ brew tap homebrew/versions
    $ brew tap homebrew/homebrew-php
    $ brew install php71
    $ export PATH="$(brew --prefix homebrew/php/php71)/bin:$PATH"
    $ php --version # PHP 7.1.11

Install composer

    $ brew install composer

Install vagrant and virtualbox
   
    # install virtualbox 5.1 from website
    $ brew cask install vagrant
    $ brew install vagrant-completion

Create a laravel project
    
    $ mkdir site
    $ cd site
    $ git init
    $ composer create-project --prefer-dist laravel/laravel blog


Add laravel homestead to the project

    $ composer require laravel/homestead --dev
    $ php vendor/bin/homestead make
    $ #generate ssh keys
    $ ssh-keygen -t rsa -b 4096 -C "dev@homestead" -f id_rsa-homestead
    $ #update the Homestead.yamland set the appropriate public and private keys

Use Vagrant to run the project

    $ vagrant up
    $ #add an entry for homestead.test in /etc/hosts 
    $ open http://homestead.test

