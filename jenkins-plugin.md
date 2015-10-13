---
title: Jenkins Plugin
---
# Jenkins Plugin

The mktmpio plugin for Jenkins integrates the mktmpio server with Jenkins so
that any build can include a dedicated database server that is created at the
start of the build and then automatically shutdown at the end. Because the
provisioning takes less than 1 second, there is virtually no impact on build
times.

<dl>
  <dt>GitHub</dt>
  <dd><a href="https://github.com/jenkinsci/mktmpio-plugin">jenkinsci/mktmpio-plugin</a></dd>
  <dt>Jenkins Plugin Page</dt>
  <dd><a href="https://wiki.jenkins-ci.org/display/JENKINS/mktmpio+Plugin">mktmpio Plugin</a></dd>
</dl>


## Usage

1. Install the mktmpio plugin for Jenkins using the Jenkins control panel
1. Create a mktmpio account by signing in with GitHub at <https://mktmp.io/>
1. Get your API key/token from <https://mktmp.io/me>
1. Enter your token into the mktmpio section of the Jenkins global config page
1. Enable mktmpio on a new or existing job
1. Select the type of database server to create
1. Modify your tests, scripts, or job actions to make use of the database
   credentials added to the build environment.

### Workflow Support

The mktmpio Jenkins plugin is also Workflow ready. Here's an example:

```Groovy
node {
  wrap([$class: 'Mktmpio', dbs: 'redis']) {
    sh 'cat seed.data | redis-cli -h $REDIS_HOST -p $REDIS_PORT -a $REDIS_PASSWORD'
    sh 'make test'
  }
}
```
