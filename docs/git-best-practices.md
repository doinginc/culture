**[⬅ Back to Coding Culture](../README.md)**

# Git Best Practices

## Branching

### The master or default branch

We should never have code in the master branch that hasn't been through code review.
Therefore work should never be directly committed to this branch.

### Creating branches

Branches should be named with the applicable ticket type and number.

This has the following benefits:

* Easy to find ticket based on the work & vice versa
* Links with Sprintly

**Bad:**

```
$ git checkout -b some-random-thing
```

**Good:**

```
$ git checkout -b STORY-12
$ git checkout -b TASK-34
$ git checkout -b DEFECT-56
$ git checkout -b TEST-78
```

## Smart Commit messages

In order for Smart Commits to work, you will need your Git Email Address to match the email address you login to [https://sprint.ly](https://sprint.ly) with.  Setting your git email address can be done on a per repository basis by editing your projects `.git/config` manually, and adding the required information under a [user] heading:

    [user]
        name = Your Name
        email = me@email.com

### Commands

#### Finding your item's number

You can easily find your item's number by hovering over it and looking underneath the circular estimator. You can find the item number in the URL of the permalink of a given item. If your item's permalink is `https://sprint.ly/product/1/item/12`, it's item number would be `12`. Sprintly looks for ticket numbers that have a pound/hash sign in front of them, such as `#12`.

#### Manipulating multiple items in a single command

You may issue a command to multiple items by separating item numbers with a comma. For instance, you could close three tickets from a single commit message with:

```
$ git commit -m 'Finished cleaning up those models and adding an admin site. Fixes #1, #2, and #3.'
```

Here's a few more examples:

* `Added blah to blah. Fixes #1.`
* `Added blah to blah. Fixes #1 and #2.`
* `Added blah to blah. Added foo to baz. Fixes #1, #4, and #2.`

**NOTE:** Item numbers are unique, auto-incrementing per product. This means that "Product A" and "Product B" can both have an item #1.

#### Executing multiple commands in a single commit

You can also execute multiple commands in a single commit. There isn't really any limit to this ability with the exception that each command will only be executed on a single ticket once. Below is an example.

```
$ git commit -m 'Added blah to foo and ripped out baz. Fixes #55. Reopens #33. Refs #4'
```

### Closing a ticket

#### Overview

From your commit message you can simply append `Fixes #12` and Sprintly will mark it as complete. This will not mark the ticket as accepted.

**Recognized keywords**

* close
* closes
* closed
* fix
* fixed
* fixes

**Example**

```
$ git commit -m 'Added a new field to the Blog model and setup South migrations. Fixes #55.'
```

### Referencing a ticket

#### Overview

Sometimes you wish to attach some notes from a commit message to an item without manipulating it. This is what Sprintly refers to as referencing an item. It will not do anything to the item other than append your note in the comments area.

**Recognized keywords**

* addresses
* re
* ref
* refs
* references
* see

**Example**

```
$ git commit -m 'Added a minified jQuery to `/static` and set up [http://daringfireball.net/projects/markdown/syntax](Markdown). References #88.'
```

### Reopening a ticket

#### Overview

Le sigh the horror of having to reopen a ticket and work on that boring code again. We feel your pain. Luckily, we've taken some of the pain out of it by allowing you to do it via your SCM/VCS of choice.

**Recognized keywords**

* breaks
* unfixes
* reopen
* reopens
* re-open
* re-opens

**Example**

```
$ git commit -m "Backed out some code that wasn't fully baked that is now breaking. Unfixes #55."
```

### Alternate Ticket Syntax

We also offer different syntax for tickets, if you're trying to integrate with other tools (e.g. Github Issues). You can reference tickets in any of the following ways:

```
#44
ticket:44
issue:44
item:44
bug:44
```

## Git ignore

Use a `.gitignore` file to exclude certain files and directories from entering the repo. We should have one `.gitignore` in root, rather than multiple across all directories.

We only need to commit the source code for our applications. There are a bunch of things that sometimes find their way into git that ideally shouldn't be there.

* Modules from package managers (e.g. `node_modules/` and `bower_components/`)
* IDE project files (e.g. `*.sublime-project` or `.idea`)
* Generated source from task runners/compilers

