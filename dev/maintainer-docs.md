# Statping-ng maintainer documentation
This document will briefly outline our workflows and give instructions on some common tasks.

Feel free to expand this; at the moment it's pretty empty here.


## GitHub actions
Binaries and docker images get built automatically by GitHub actions.
If the builds succeed, tests are run to ensure nothing is completely broken.
Build artifacts can be downloaded from the actions tab on GitHub.

This happens on every push to this repo and on every pull request update.


## Releases
We used to have a model of "stable" and "unstable" releases, which would get triggered by pushing to a respective release branch.
The new system tries to address some of the issues with the old system and simplifies the workflow definitions.

Incoming pull requests are merged into the `main` (default) branch.
Once you feel like we have enough new changes to justify a release, a tag can be created.
This is **not** a GitHub release and sadly can't be done from github.com directly.
Either
* create a stable release ready for general usage as `v{major}.{minor}.{patch}`, e.g. `v1.2.3`
* or create a beta release intended for testing as `v{major}.{minor}.{patch}-{suffix}`, e.g. `v1.2.3-rc0`
  * personal note: I don't know what a good format for suffixes is. I'm not even sure if we _need_ beta releases long term. We'll see; I'm open to suggestions

To create a tag from your local workspace, run
```bash
git checkout main
git pull
git tag v1.2.3
git push origin v1.2.3
```
You can also create tags on different branches (e.g. for backports).
Remember to check out the revision you want to tag _before_ tagging.
Do not move existing (pushed) tags!

When a new tag is pushed, the same build+test actions described above run, but additionally the built docker images are pushed and a draft release on GitHub is created.
All artifacts will get attached to that release.

The release will be in draft mode to allow last minute changes if necessary.
Untick the draft checkbox if everything looks alright.
