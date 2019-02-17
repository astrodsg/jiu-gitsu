

## Task-1 db migrations
Implement a tool for running database migrations


## Task-2 github external ids migration

change github_user/issue/issue_event to use the external id as the primary key... This will make lookups between source much easier. Or maybe index unique? Update pipeline


## Task-3 implement airflow for etl

update download_events:
 1. download issues
 1. etl issues into db
 1. query db for issues, github_issue.last_events_fetch_at < min or null
 1. get events for issues
 4. store data_lake and update github_issue.last_events_fetch_at

Data Pipeline
1. download_issues.py
1. etl_github_repo.py
1. etl_github_users.py
1. etl_github_issues.py
1. download_github_issue_events.py


## Task-4 create separate gitsu-etl and gitsu-analytics

Rename gitsu to gitsu-etl
Create new gitsu-analytics project
Remove all analytics components from gitsu-etl


## Task-5 create gitsu-web

For API web access.