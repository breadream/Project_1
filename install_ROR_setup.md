## Install Homebrew
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install Ruby 
```
brew install rbenv ruby-build
```


### Add rbenv to bash so that it loads every time you open a terminal
```
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile<br />
source ~/.bash_profile
```

### Install Ruby
```
rbenv install 2.5.1
rbenv global 2.5.1
ruby -v
```
 
## Configure Git 
```
git config --global color.ui true
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR@EMAIL.com"
ssh-keygen -t rsa -C "YOUR@EMAIL.com"
```

#### Copy & Paste the output of the following command 
```
cat ~/.ssh/id_rsa.pub 
```
-> 
https://github.com/settings/keys
#### Check if it works
```
ssh -T git@github.com
```

## Install Rails 
```
gem install rails -v 5.2.0
rbenv rehash
rails -v
```

## Setup Database
```
brew install sqlite3
```
## Install mysql
```
brew install mysql
```
## Run mysql

## To have launchd start mysql at login:
```
brew services start mysql
```


### Create Rails Application
```
rails new myapp
```
- if it shows 'Errno::EACCES: Permission denied @ dir_s_mkdir', go into myapp folder and do 'sudo bundle install'

### If you want to use MySQL
```
rails new myapp -d mysql
```

### Move into the application directory
```
cd myapp
```

- If you setup MySQL or Postgres with a username/password, modify the config/database.yml file to contain the username/password that you specified

### Create the database
```
rake db:create
rails server
```

