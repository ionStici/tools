[&larr; Back](./README.md)

# Git Behind the Scenes

Git is a **key-value data store**. We can insert any kind of content into a git repo, and git will hand us back a unique key we can later use to retrieve that content. These keys that we get back are SHA-1 checksums.

## What is in `.git`

- `config` file is for configuration. Besides global configurations, we can configure per-repo basis.

- Inside `refs` folder, you'll find a `heads` directory.

  `refs/heads` contains one file per branch in a repo. Each file is named after a branch and contains the hash of the commit at the tip of the branch.

  e.g. `refs/heads/master` contains the commit hash of the last commit on the master branch.

  `refs` also contains a `refs/tags` folder which contains one file for each tag in the repo.

- `HEAD` is a text file that keeps track of where HEAD points.

  If it contains `refs/heads/master`, this means that HEAD is pointing to the master branch.

  In detached HEAD, the HEAD file contains a commit hash instead of a branch reference.

- `index` file is a binary file that contains a list of the files the repo is tracking. It stores the file names as well as some metadata for each file.

- `objects` directory contains all the repo files. This is where git stores the backups of files, the commits in a repo, and more.

  The files are all compressed and encrypted, so they won't look like much.

<br>

## 4 types of Git objects

- **Annotated tag**

- Git **blobs** (binary large object) are the object type git uses to store the **contents of files** in a given repo. Blobs don't even include the filenames of each file or any other data. They just store the contents of a file.

- **Trees** are git objects used to store the contents of a directory. Each tree contains pointers that can refer to blobs and to other trees.

  Each entry in a tree contains the SHA-1 hash of a blob of tree, as well as the mode, type, and filename.

- **Commit** objects combine a tree object along with information about the context that led to the current tree. Commits store a reference to parent commit(s), the author, the commiter, and the commit message.

<br>
