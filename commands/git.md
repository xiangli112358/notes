# Git Commands

## Tagging

### List tags
Listing tags in repository is quite simple, just type `git tag`:

```
git tag
```
You can use the `-l` option to list tags.  `*` wildcard can be used to match some pattern, the example below will only list released tags:

```
git tag -l *Final*
```

### Create tags
You can create tags by using the `-a` option. Additional message associated with the tag can be specified by using the `-m` option.

```
git tag -a <tag name> -m <tag message>
```