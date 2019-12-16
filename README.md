# jira
Add a new Jira card for a Bugzilla bug.

## Requirements
* bash
* [jq](https://stedolan.github.io/jq/)


## Configuration
* environment variable `JIRA_USERNAME` (or flag `-u`): Your Red Hat account username
* environment variable `JIRA_PASSWORD` (or flag `-p`): Your Red Hat password


## Use
```
./jira bz new [-s] <bz_id>...
```

`-s`: add the Jira card to the current sprint.

## Examples
This will create Jira cards for Bugzillas 1, 2 and 3:

```
./jira bz new 1 2 3
```

This will create Jira cards for Bugzillas 1, 2 and 3 and add them to the current sprint:

```
./jira bz new -s 1 2 3
```
