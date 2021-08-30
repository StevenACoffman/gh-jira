## gh-jt extension

This GitHub extension lets you manipulate JIRA issues. For instance, to transition JIRA issue TEAM-1234 to "In Progress" State:
```
gh jira "In Progress" TEAM-1234
```

You must have installed [jt](https://github.com/StevenACoffman/jt) for it to work.


If you are in a git repository where the topic branch's name matches `[whatever-]team-1234[-whatever]`, you can omit
the issue argument as it is implied.

Yeah, we even let you use underscores!

### Synopsis

GitHub CLI extensions are repositories that provide additional gh commands.

The name of the extension repository must start with "gh-" and it must contain an executable of the same name. All arguments passed to the `gh <extname>` invocation will be forwarded to the `gh-<extname>` executable of the extension.

An extension cannot override any of the core gh commands.

### Wait, this is just a bash wrapper for some other tool?

Yeah, GitHub CLI binary extensions won't install properly yet. See [github.com/cli/cli#4194](https://github.com/cli/cli/issues/4194). 
Once it can, we can move the Go code here.