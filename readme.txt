Hi all
I hope you enjoyed today's session and things were pretty clear
Until the next session please work on this assignment:
Write user data script that will help you automating chef execution
You can use the cookbook from our session for this assignment.
the script should:
install chefdk
install git
clone your git repository (that has all needed cookbooks & configurations)
execute chef-solo
Additionally - come with a final idea for your project.
See you next week :cloudschool:

#!/bin/bash
sudo -i
apt update
apt install git wget https://packages.chef.io/files/stable/chefdk/4.13.3/ubuntu/20.4/chefdk_4.13.3-1_amd64.deb dpkg --install
chefdk_4.13.3-1_amd64.deb git init
mkdir chef_from_git
cd chef_from_git
git init
git remote add origin -f https://github.com/matanelelimelech/chef-user-data.git
.git/info/sparse-checkout
git pull origin master
chef-solo -c /chef/singl.rb -j /chef/go.json
