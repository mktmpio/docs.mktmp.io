---
title: Slack Integration
---
# Slack Integration

You can add mktmpio to your Slack team and allow anyone on your team to
interact with the mktmpio service using a `/mktmpio` slash command.

If you already have a Slack team and you already have a mktmpio account,
setting up the integration is simple!

1. Make sure you are logged in to https://mktmp.io/
2. Make sure you are logged in to your Slack team
3. <a href="https://slack.com/oauth/authorize?scope=commands&client_id=17105111350.17367841751&redirect_uri=https://mktmp.io/auth/slack/callback"
   ><img alt="Add to Slack" height="40" width="139"
     src="https://platform.slack-edge.com/img/add_to_slack.png"
     srcset="https://platform.slack-edge.com/img/add_to_slack.png 1x, https://platform.slack-edge.com/img/add_to_slack@2x.png 2x"></a>
4. That's it, you should now have a `/mktmpio` command available in Slack!

## Usage

### Help

You can run `/mktmpio` with no commands and it will respond with usage
instructions. Don't worry about spamming your channels, your command
*and* the output from this are visible only to you!

```
Usage: /mktmpio <command>
Commands:
  create,new TYPE      create a new instance of type TYPE
  ls,list              list currently runnning instances
  get ID               get details of a specofic instance ID
  rm,delete ID         terminate instance ID
```

### Creating Databases

Just like the `mktmpio` CLI, you can do `/mktmpio new redis` and you'll get
a response back with all the details of the newly created server.

### Listing Databases

You can use `/mktmpio ls` to get a list of all of your currently running
databases, including full details.

### Deleting Databases

Once you are finished with a database, simply delete it with `/mktmpio rm ID`,
giving it the instance ID for the instance as given when it was created or
from running `/mktmpio ls`.
