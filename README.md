bitbucket_pr_commnet
===

[![Gem Version](https://badge.fury.io/rb/bitbucket_pr_commnet.svg)](https://badge.fury.io/rb/bitbucket_pr_commnet)

post comment to pull requiest on bitbucket

## Require
* git

## Install

```bash
$ gem install bitbucket_pr_commnet
```

## Setup
Get the bitbucket consumer key.  

[OAuth on Bitbucket Cloud](https://confluence.atlassian.com/bitbucket/oauth-on-bitbucket-cloud-238027431.html)

* Callback URL: `urn:ietf:wg:oauth:2.0:oob`
* Check `This is a private consumer`

Pleasse make sure the consumer key and secret.

## Usage
Set the client_id and client_secret to arguments or environment variables.
And, please specify a comment by the filename or pipe.

Exaple:
```
$ cat comment_file
Pull request commnet test!
$ bitbucket_pr_commnet comment_file --client_id xxxx --client_secret xxxx
```

OR

```
$ export CLIENT_ID=xxxx
$ export CLIENT_SECRET=xxxx
$ cat comment_file
Pull request commnet test!
$ cat comment_file | bitbucket_pr_commnet
```

## License
MIT
