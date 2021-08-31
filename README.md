1. git show aefea
   commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
   Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>
   Date:   Thu Jun 18 10:29:58 2020 -0400

       Update CHANGELOG.md

2. git show 85024d3
   commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)

3. git show -s --pretty=%P b8d720
   2 parents:
   58dcac4b798f0a2421170d84e507a42838101648 
   ffbcf55817cb96f6d5ffe1a34abe963b159bf34e
 
4. git log --oneline v0.12.23..v0.12.24
   b14b74c49 [Website] vmc provider links
   3f235065b Update CHANGELOG.md
   6ae64e247 registry: Fix panic when server is unreachable
   5c619ca1b website: Remove links to the getting started guide's old location
   06275647e Update CHANGELOG.md
   d5f9411f5 command: Fix bug when using terraform login on Windows
   4b6d06cc5 Update CHANGELOG.md
   dd01a3507 Update CHANGELOG.md
   225466bc3 Cleanup after v0.12.23 release
5. git log -S "func providerSource"
   commit 8c928e83589d90a031f811fae52a81be7153e82f
   Author: Martin Atkins <mart@degeneration.co.uk>
   Date:   Thu Apr 2 18:04:39 2020 -0700

6. git log -L :globalPluginDirs:plugins.go --oneline 
   78b122055 Remove config.go and update things using its aliases
   52dbf9483 keep .terraform.d/plugins for discovery
   41ab0aef7 Add missing OS_ARCH dir to global plugin paths
   66ebff90c move some more plugin search path logic to command
   8364383c3 Push plugin discovery down into command package
7. git log -G synchronizedWriters --oneline
   git checkout 5ac311e2a
   git grep -p "synchronizedWriters"
   git log -L :synchronizedWriters:synchronized_writers.go
   commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5 (HEAD)
   Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Wed May 3 16:25:41 2017 -0700
