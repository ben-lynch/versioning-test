# Versioning Test

Test repo to figure out branching, tagging.

New branch made to patch this release

- Potential command: `git describe --tags --abbrev=0 HEAD`
  Gets the closest single tag, from the head. However this may not work if other tags are present.
  Edit: Indeed that is the case, a tag made on "Commit 2" with the sha (as seems ot be how it is done) appears as the tag listed.

  ```
    $ git tag -a "release/2769d60" -m "release sha: release/2769d60" 2769d60
    $ git describe --tags --abbrev=0 HEAD
    release/2769d60
  ```
