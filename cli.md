---
title: mktmpio CLI
---
# CLI

This is the `mktmpio` command.

<dl>
  <dt>Binaries</dt>
  <dd><a href="https://github.com/mktmpio/cli/releases/latest">Mac OS X, Windows, Linux</a></dd>
  <dt>GitHub</dt>
  <dd><a href="https://github.com/mktmpio/cli">mktmpio/cli</a></dd>
</dl>

```man
NAME:
   mktmpio - create, destroy, and manage mktmpio database servers

USAGE:
   mktmpio [global options] command [command options] [arguments...]

GLOBAL OPTIONS:
   --token "TOKEN"	API token for making requests to mktmpio service [$MKTMPIO_TOKEN]
   --url "URL"		override the URL for the mktmpio service [$MKTMPIO_URL]
   --help		show help
   --version		print the version

COMMANDS:
   config	view and modify your mktmpio config
   ls		list and inspect running database servers
   rm		shutdown running database servers
   shell	create a new server and attach a shell session to it
   legal	display licensing, copyright, and warranty notices
   help, h	Shows a list of commands or help for one command

BUGS:
   Report to https://github.com/mktmpio/cli/issues

VERSION:
   Version: 0.7.0
   Compiled: 2016-01-10 23:52:41 +0000 UTC

COPYRIGHT:
   Copyright 2015 Datajin Technologies, Inc.
```
