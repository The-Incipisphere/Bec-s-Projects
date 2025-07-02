A small CLI tool that i'm gonna make when i set up my linux pc
# Premise
basically a version of `rm` that makes it much harder for me to shoot myself in the foot, by warning me if i'm trying to affect:
- more than X total files/dirs
- more than Y total MiB of data
- any files/dirs on a list Z (for example: `/bin/`, `/root/`, `/boot/`, `/lib/`, `/etc/`)

and it would default to putting the things in `~/.local/share/Trash/` unless it can't (in which case it will state which files/dirs couldn't be affected), or a user set their trash dir elsewhere

if needs be, there would be at least these two flags:
- `--dont-warn-for-big-actions` to skip the warning prompt even if any of the earlier mentioned criteria return true - used for things like CI/CD
- `--bypass-the-trash-bin` to explicitly pass through to standard `rm` then and there - ***Would be used SPARINGLY.***