# jira

Add a new Jira card for a Bugzilla bug.

## Required configuration

* `JIRA_USERNAME`   (or flag `-u`): Your Kerberos ID, without the '@redhat.com' part.
* `JIRA_JSESSIONID` (or flag `-p`): Look into your browser's cookies..


## Use
```
./jira bz <bz_id>
```

## Examples

This command will create a Jira card with summary `BZ-123`, with the link to the BZ in the description:

```
./jira bz 123
```


