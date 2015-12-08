# utility_commands

This repository has commands I use for making stuff easier for myself.

To make this use full add `~/utility_commands/bin` to your `PATH`.

* [cibot-pull][cibot-pull]: Copies command to clipboard that is used to make a pull request for CIBot.
* [git_rm_local][git_rm_local]: Removes all local branches that are safe to remove.
* [push-origin][push-origin]: Alias for `git push origin CURRENT_BRANCH`.
* [branch-commit][branch-commit]: Alias for `git commit -m "BRANCH_NAME - MESSAGE"`, where `MESSAGE` is passed as a command line string.
* [git-attempt-recovery][git-attempt-recovery]: This is an alias for an awesome command. It makes it easy to track down "lost" commits in your git repository. Useful if you've deleted something by accident and want to find it again. Alias command: `git fsck --unreachable | grep commit | cut -d\  -f3 | xargs git log --merges --no-walk --grep=WIP`
* [hipchat-message][hipchat-message]: This allows you to send a message to hipchat see below for setup and example.


## Setup

### hipchat-message

The hipchat-message command requires the following:

1. The python [requests][requests-library] library. (`pip install requests`)
1. An environment variable `HIPCHAT_MESSAGE_TOKEN`. You can generate that [here][hipchat-token-url]
2. Pass a message to the command: `echo "testing the cli" | hipchat-message`

Right now the room is hardcoded to where I want to post my automated messages. If you work at C2FO this may
work well for you too.

Command I actually use:

`cibot-pull | hipchat-message`

[cibot-pull]: bin/cibot-pull
[git_rm_local]: bin/git_rm_local
[push-origin]: bin/push-origin
[branch-commit]: bin/branch-commit
[git-attempt-recovery]: bin/git-attempt-recovery
[hipchat-message]: bin/hipchat-message
[hipchat-token-url]: https://c2fo.hipchat.com/account/api
[requests-library]: http://docs.python-requests.org/en/latest/
