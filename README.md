bitbucket-plugin
================

**NOTE:** This was an early attempt at getting bitbucket webhooks to do what I wanted (eg. be more dynamic and scriptable). Turns out the [Generic Webhook Plugin](https://wiki.jenkins.io/display/JENKINS/Generic+Webhook+Trigger+Plugin) is a vastly superior option that works with any service that will post data in reasonable formats - for my purposes anyway.

[![Build Status](https://jenkins.ci.cloudbees.com/job/plugins/job/bitbucket-plugin/badge/icon)](https://jenkins.ci.cloudbees.com/job/plugins/job/bitbucket-plugin/)

See details on [wiki](https://wiki.jenkins-ci.org/display/JENKINS/BitBucket+Plugin)

# Job DSL
The plugin supports the following dsl extension to enable bitbucket pushes to trigger a build:

```
freeStyleJob('test-job') {
  triggers{
    bitbucketPush()
  }
}
```
