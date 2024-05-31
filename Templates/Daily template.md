---
tags: daily
---
Things for {{date:dddd Do MMMM}}

## Tasks
*Think about things that need to get done*
- [ ]

## Meetings
*May take time to load*

<%* var events = await app.plugins.getPlugin('ics').getEvents(moment(tp.file.title,'YYYY-MM-DD')); events.sort((a,b) => a.utime - b.utime).forEach((e) => { tR+=`**${e.time}:**  ${e.summary} ${e.location? e.location : ''}\n` }) %>

## Misc
_Capture random things here_
## Review Jira
_Review Jira tickets assigned to or mentioning me_
### Assigned
```jira-search
query: assignee = currentUser() AND resolution = Unresolved AND statusCategory = "In Progress"
columns: KEY, SUMMARY, -ASSIGNEE, -REPORTER, STATUS
```
### Mentions
```jira-search
query: text ~ currentUser() AND resolution = Unresolved AND statusCategory = "In Progress"
columns: KEY, SUMMARY, -ASSIGNEE, -REPORTER, STATUS
```

## Review GitHub

```github-query
outputType: table
queryType: pull-request
query: repo:EnterpriseDB/upm-rfcs is:pr state:open
columns: [number, title, author, updated]
```
