# Git Tags

Git Tags are pointers that refer to particular points in Git history. We can mark a particular moment in time with a tag. Tags are most often used to mark version releases in projects.

Think of tags as branch references that do not change. Once a tag is created, it always refers to the same commit. It's just a label for a commit.

_Two types of git tags:_

- **lightweight tags** - name / label that points to a particular commit.

- **annotated tags** - store extra meta data including the author's name and email, the date, and a tagging message.

## Semantic Versioning

The semantic versioning spec outlines a standardlized versioning system for software releases. It provides a consistent way for developers to give meaning to their software releases.

Versions consists of 3 numbers separated by dots.

- **Initial Release:** `1.0.0` - the first release

- **Patch Releases:** `1.0.1` - normally do not contain new features or significant changes. They typically signify bug fixes and other changes that do not impact how the code is used

- **Minor Release:** `1.1.0` - minor releases signify that new features or functionality have been added, but the project is still backwards compatible. No breaking changes. This new functionality is optional and should not force users to rewrite their own code.

- **Major Release:** `2.0.0` - major releases signify changes that is no longer backwards compatible. Features may be removed or changes substantially.

- **Example:** `2.5.1` - major / minor / patch

- **Early stages:** `0.0.1` - signals that the software is in its early stages of development, meaning initial development, where the software is being built and might be unstable or incomplete.

## Tags in Practice

- `git tag` print a list of all the tags in the current repo.

- `git tag -l keyword` search for tags that match a particular pattern using `-l` option.

- `git checkout <tag>` (detached HEAD) view the state of the repository at a particular tag.

- `git tag <tagname>` create a lightweight tag, referring to the current HEAD commit.

- `git tag -a <tagname>` create an annotated tag. Use `-m` option to pass a message directly.

- `git show <tagname>` display the tag annotation, the corresponding commit information, and a diff of the changes that were committed in that tag.

- `git tag -v <tagname>` only for the annotation and commit data, without the diff

- `git tag <tagname> <commit-hash>` tag a particular commit using the commit hash.

- `git tag -f <tagname>` force a tag.

- `git tag -d <tagname>` delete a tag.

- `git push --tags` push all of your tags to the remote server.

  By default, `git push` doesn't transfer tags to remote servers.
