# Versioning Test

Test repo to figure out branching, tagging.

New branch made to patch this release

- Potential command: `git describe --tags --abbrev=0 HEAD`
  Gets the closest single tag, from the head. However this may not work if other tags are present.
  Edit: Indeed that is the case, a tag made on "Commit 2" with the sha (as seems ot be how it is done) appears as the tag listed.

  ```shell
    $ git tag -a "release/2769d60" -m "release sha: release/2769d60" 2769d60
    $ git describe --tags --abbrev=0 HEAD
    release/2769d60
  ```

Current state of play:

```shell
* 3fda9ed (HEAD -> new-patch-release, origin/new-patch-release) Commit 10
* e18719f Commit 9
* bf18a38 Commit 8
| * 976db01 (origin/main, origin/HEAD, main) Commit 7
| * 897a94a Commit 6
| * b6b5066 (tag: release/0.2.3.1) Commit 5
| * b65772e Commit 4
| * ce206a0 (tag: release/0.1.2.1) Commit 3
| * b523b24 Commit 2
|/
* 2769d60 (tag: release/2769d60, tag: release/0.1.1.1) Commit 1
* e130a29 Initial commit
```

This command might work: `git describe --tags --abbrev=0 --match "release/*.*.*.*" HEAD`

Going to test with that one.
