### MRs PRs and how can we make life of code reviewers easy

bigger MRs = more commits = more code change = (possibly) more review comments = (possibly) even more code changes in that MR and more commits = even more time getting it reviewed and merged = lot more attention needed from reviewer all this time = (maybe) less confidence in code? = (maybe) more chances of bugs?

How to make MRs easy for reviewer's and as a side effect to make code history usable
* Look for creating small MRs made with small commits. Smaller MRs are easier to review as well as easier to track and rollback.
* We don't want code of whole feature as single MRa.
* Many small commits in MR are lot better than single large commit.
* Every commit should do only one thing - or things that are very closely related to each other.
* Commit is not just "bunch" of code changes. It should only do what commit message indicates. If you are not able to write single line summary of what changes are done in given commit, may be your commit is doing lot many things at ones.
* Try to put relevant commit messages. Commit messages help a lot in review - even if someone is out of touch or doesn't have context.
* Always put code along with corresponding tests in single commit. Helps understand purpose of code.
* Avoid code movement, renaming, refactoring etc. and adding new functionality or updating logic of existing functionality in single commit. It makes the whole thing very confusing as it mixes whats added and whats moved/renamed.
* If particular part of code change request in MR is getting tricky, more than estimated time, feel free to create separate issue and address it in a separate MR. Just putting more stuff in same MR is not good solution.
* Please consider that reviewer is looking at multiple MRs, may be from different parts of code. So provide enough context and references when replying to comments.
* Make sure you reply to each review request/comment by separate commit hash containing that change. If change is not very trivial, ideally wait for reviewer's +1.
* While addressing suggestions in review requests/comment, feel free to combine multiple requests in single commit only if they are related. Otherwise, separate commit for separate request makes it very easy for reviewer to track what changed.
* If particular MR is getting complex while addressing review requests/comments, or if there is change in the way implementation is done, please close the MR and opens separate MR.
* `git rebase -i` is your friend.
* Read your own code before finally publishing review request.

Side notes
* There could be argument between whether to squash all the commits when MR is merged. I am of the opinion that don't squash. If commits are written in good style, having separate commits just makes it lot easier look through code history and pin-point to any change when some bug occurs.
* Build culture that makes code reviewes enjoyable and way of having healthy discussion about various programming/software-engineering topics.
* Code reviews could be great way to learn more about parts of codebase which you have not touched.
* Showcase/share beautifully crafted MRs with wider team. It highlights importance of better code and better reviews and politely hinting everyone to go for it.

These are some things I have learned over years and have worked well in many teams. Obviously, these are not "rules" to follow exactly as is by everyone. Every team will have (or should have) their own version around similar points.
