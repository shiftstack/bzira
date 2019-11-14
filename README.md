# jira

## Use

Add a new Jira card in the sprint for a Bugzilla bug.
Required configuration:
* `JIRA_COOKIE` (or flag `--cookie`): The Jira web cookie 'JSESSIONID'.
* `JIRA_USERNAME` (or flag `--username`): Your Kerberos ID, without the '@redhat.com' part.

This command will create a Jira card with summary `BZ-123`, with the link to the BZ in the description:

```
./jira bz 123
```


