# This repository is forked by [Bilendo.de](http://www.bilendo.de)
original repository: https://github.com/forward3d/cap-ec2

---

### Changes:
- fixed `YAML.load` command in `CapEC2::Utils#load_config`
- require `aws-sdk-ec2` instead of whole sdk


### Installation:
- add `gem 'cap-ec2', git: 'https://github.com/bilendo/cap-ec2.git'` to your `Gemfile`
- add `require 'cap-ec2/capistrano'` to your `Capfile`
- run `bundle exec cap production ec2:status` to view your instances


### Global Installation:
If you want to directly call `cap stage <command>` without the bundler prefix,  
install the gem globally:
```bash
git clone git@github.com:bilendo/cap-ec2.git
cd cap-ec2.git
gem uninstall cap-ec2 # uninstall previous versions
gem build cap-ec2.gemspec
gem install cap-ec2-1.1.2.gem
```

**Hint:**  
Make sure to select the right Ruby version.  
Change the version of `.ruby-version` if you use `rbenv`.  
If you use `rvm` – don't!
