[![Build Status](https://travis-ci.com/shiftstack/bzira.svg?branch=master)](https://travis-ci.com/shiftstack/bzira)
# jira
Add a new Jira card for a Bugzilla bug.

## Requirements
* bash
* [jq](https://stedolan.github.io/jq/)


## Configuration
* environment variable `JIRA_USERNAME` (or flag `-u`): Your Jira username as found in your [Jira profile](https://issues.redhat.com/secure/ViewProfile.jspa)
* environment variable `JIRA_PASSWORD` (or flag `-p`): Your Red Hat developer account password


## Use
```
./bzira bz new [-s] <bz_id>...
```

`-s`: add the Jira card to the current sprint.

## Examples
This will create Jira cards for Bugzillas 1, 2 and 3:

```
./bzira bz new 1 2 3
```

This will create Jira cards for Bugzillas 1, 2 and 3 and add them to the current sprint:

```
./bzira bz new -s 1 2 3
```
