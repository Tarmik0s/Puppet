Download rpm fle then install packages
rpm -Uvh https://yum.puppetlabs.com/puppetlabs-release-pc1-el-7.noarch.rpm 
yum -y install puppetserver gcc-c++ patch readline readline-devel zlib zlib-devel libyaml-devel libffi-devel openssl-devel make bzip2 autoconf automake libtool bison iconv-devel sqlite-devel 

Download RVM for the Puppet to use hiera YAML data

curl -sSL https://rvm.io/mpapis.asc | gpg --import - 
curl -L get.rvm.io | bash -s stable  
source /etc/profile.d/rvm.sh 
rvm reload 
rvm requirements run 
rvm install 2.2.4 
rvm use 2.2.4 --default 
ruby –version 
Gem install hiera 
