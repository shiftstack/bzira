# jira

Add a new Jira card for a Bugzilla bug.

## Required configuration

* `JIRA_USERNAME`   (or flag `-u`): Your Kerberos ID, without the '@redhat.com' part.
* `JIRA_JSESSIONID` (or flag `-p`): Look into your browser's cookies..


## Use
```
./jira bz [-s] <bz_id>...
```

`-s`: add the Jira card to the current sprint.


## Examples

This command will create Jira cards for Bugzillas 1, 2 and 3:

```
./jira bz 1 2 3
```

This command will create Jira cards for Bugzillas 1, 2 and 3 and add them to the current sprint:

```
./jira -s bz 1 2 3
```
