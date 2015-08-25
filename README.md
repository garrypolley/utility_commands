# utility_commands

This repository has commands I use for making stuff easier for myself.

To make this use full add `~/utility_commands/bin` to your `PATH`.

* [cibot-pull][cibot-pull]: Copies command to clipboard that is used to make a pull request for CIBot.
* [git_rm_local][git_rm_local]: Removes all local branches that are safe to remove.
* [push-origin][push-origin]: Alias for `git push origin CURRENT_BRANCH`.
* [branch-commit][branch-commit]: Alias for `git commit -m "BRANCH_NAME - MESSAGE"`, where `MESSAGE` is passed as a command line string.

[cibot-pull]: bin/cibot-pull
[git_rm_local]: bin/git_rm_local
[push-origin]: bin/push-origin
[branch-commit]: bin/branch-commit
