# scripts

These are some scripts I use to automate my workflow!

### dependencies

My scripts make heavy use of [charmbracelet/gum](https://github.com/charmbracelet/gum), so go ahead and install that!

On Arch, it's just `pacman -S gum`.

#### gitaccount

This is a simple script used to switch git identities in a pinch! It supports changing the properties: `user.name`, `user.email`, and `user.signingkey`. To use it, simply create the file `~/.config/gitaccounts.csv` according to the following template:

```csv
Name,Email,Signing Key
William Shakespeare,wshaker@thisdomaindoenotexist.com,0123456789ABCDEF0123456789ABCDEF
dactylichexameterfan12,microtonal@englishmail.monster,0123456789ABCDEF0123456789ABCDEF
```

You can opt to omit the signing key, just make sure it stays a part of the csv schema, though! The script can be used in two ways: by switching the global identity for git or switching the identity on a per-repository basis. By default, running the script (not in a git repository) will prompt you to see if you would like to run the command globally (just to confirm!). While in a git repository, the command will only run affecting the current git repository.

#### gitcommit (wip?)

Stupid simple script inspired by the gum examples that is used to author git commits with some sort of silly convention thing.

It's kind of bad in its current state and use it to your own peril, I guess :D
