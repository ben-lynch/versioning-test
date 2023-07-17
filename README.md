# Versioning Test

Test repo to figure out branching, tagging via git commands.

- List tags: `git tag`
- Create tag: `git tag -a "release/0.1.1.1" -m "release version label: release/0.1.1.1"` (matches the first release)
- Push tags: `git push --tags`
- Get last tag (on branch or main) matching the release tag pattern: `git describe --tags --abbrev=0 --match "release/*.*.*.*" HEAD`

The above command looks like a winner.

```shell
* 8e0f8b6 (HEAD -> main, origin/main, origin/HEAD) Commit 12
* 976db01 Commit 7
* 897a94a Commit 6
* b6b5066 (tag: release/0.2.3.1) Commit 5
* b65772e Commit 4
* ce206a0 (tag: release/0.1.2.1) Commit 3
* b523b24 Commit 2
| * 6f15e5d (origin/new-patch-release, new-patch-release) Commit 11
| * 3fda9ed Commit 10
| * e18719f (tag: release/0.1.1.2) Commit 9
| * bf18a38 Commit 8
|/
* 2769d60 (tag: release/2769d60, tag: release/0.1.1.1) Commit 1
* e130a29 Initial commit
```
