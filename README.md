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

# branch  commands
su redmine

cd ~/redmine/plugins && git clone https://github.com/kaikuo/issue_id.git && cd issue_id && git checkout -t origin/autoid && cd ../..  && bundle exec rake redmine:plugins:migrate RAILS_ENV=production

bundle exec rake redmine:plugins:migrate RAILS_ENV=production

bundle exec rake redmine:plugins:migrate RAILS_ENV=development

Restart Redmine/ChiliProject
