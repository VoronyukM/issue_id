# Change log

try to change parent_issue_id when create

# info

https://github.com/kaikuo/issue_id.git

fork from 

https://github.com/VoronyukM/issue_id

# Installation notes

Copy issue_id directory to: #{RAILS_ROOT}/plugins
Run: 

# docker iamges

sameersbn/postgresql:9.4-23
sameersbn/redmine:2.6.1

# master commands

su redmine

cd ~/redmine/plugins && git clone https://github.com/kaikuo/issue_id.git && bundle exec rake redmine:plugins:migrate RAILS_ENV=production


https://git.oschina.net/kzhuo/issue_id.git

# branch  commands
su redmine

cd ~/redmine/plugins && git clone https://github.com/kaikuo/issue_id.git && cd issue_id && git checkout -t origin/autoid && cd ../..  && bundle exec rake redmine:plugins:migrate RAILS_ENV=production

bundle exec rake redmine:plugins:migrate RAILS_ENV=production

bundle exec rake redmine:plugins:migrate RAILS_ENV=development

Restart Redmine/ChiliProject

# new plugins

git clone https://github.com/javiferrer/redmine_import_issues.git
git clone https://github.com/two-pack/redmine_xlsx_format_issue_exporter.git

gem sources -r https://rubygems.org/
gem sources -a https://ruby.taobao.org/

bundle install && bundle exec rake redmine:plugins:migrate RAILS_ENV=production
