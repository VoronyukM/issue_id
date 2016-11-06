# Change log

0.0.2
Fix: Error 404 when copy an issue with ISSUE-id
Fix: Can not deal issue id when adding a subtask 
Fix: Git repository parsing fails if there was not specified any fix keywords in Redmine settings

# info

Sequent issue numbers are easier to remember. While Redmine does uses sequent numbers for issues they are sequent not in the project scope. Therefore on installations with large number of projects we are getting random-like increasing numbers for a project’s issues.

The majority of Redmine competitors support sequent per-project issue numbers by prepending specific project prefixes like REDMINE-. This plugins does the same for Redmine! At the same time the native issue numbering style continues to work fine.

*P.S. When moved the issue prefix and number get changed, but still the previous issue id continues to work by redirecting to the new one.*

# Installation notes

```
cd /path/to/redmine/
git clone https://github.com/VoronyukM/issue_id.git
bundle exec rake redmine:plugins:migrate RAILS_ENV=production
```

Restart the Redmine/ChiliProject


To uninstall the plugin migrate the database back and remove the plugin:
TODO

Further information about plugin installation can be found at: http://www.redmine.org/wiki/redmine/Plugins
