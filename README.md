[![Build Status](https://travis-ci.com/shiftstack/bzira.svg?branch=master)](https://travis-ci.com/shiftstack/bzira)
# jira
Add a new Jira card for a Bugzilla bug.

## Requirements
* bash
* [jq](https://stedolan.github.io/jq/)


## Configuration
* environment variable `JIRA_USERNAME` (or flag `-u`): Your Jira username as found in your [Jira profile](https://issues.redhat.com/secure/ViewProfile.jspa)
* environment variable `JIRA_PASSWORD` (or flag `-p`): Your Red Hat developer account password

Note on password complexity: **This tool authenticates against the Jira instance using Basic Auth, which [does not support non US-ASCII characters](https://tools.ietf.org/html/rfc7617#page-8)**.

## Use

### Add a new issue for a Bugzilla

```
./bzira bz new [-s] <bz_id>...
```

`-s`: add the Jira card to the current sprint.

Example 1: This will create Jira cards for Bugzillas 1, 2 and 3:

```
./bzira bz new 1 2 3
```

Example 2: This will create Jira cards for Bugzillas 1, 2 and 3 and add them to the current sprint:

```
./bzira bz new -s 1 2 3
```

### Add a Github Pull Request link to a Jira card

```
./bzira issue pr <issue_key> <pr_url>
```

Example:

```
./bzira issue pr OSASINFRA-1015 'https://github.com/openshift/installer/pull/3128'
```

### Add a Bugzilla link to a Jira card

```
./bzira issue bz <issue_key> <bz_id>
```

Example:

```
./bzira issue bz OSASINFRA-1315 1804083
```
