doubledown(1) -- sync local changes to a remote directory
=========================================================

## SYNOPSIS

`doubledown` _local_ [_user_@]_server_:_remote_

## DESCRIPTION

`doubledown` brings _local_ and _remote_ on _server_ into sync and then executes doubledown-fsevents(1) to watch _local_ for changes.

An ssh-agent(1) is started if one cannot be found.

rsync(1) is used to first download all files in _remote_ on _server_ that do not exist in _local_, thus no local changes will be clobbered.  It then uploads any local changes.

## OPTIONS

* `-h`, `--help`:
  Show a help message.

## THEME SONG

The Arcade Fire - "The Suburbs"

## AUTHOR

Richard Crowley <richard@devstructure.com>

## SEE ALSO

`doubledown` was written to make it easier for DevStructure users to use Textmate and other IDEs but it's far from the only way to skin the cat.  See <http://docs.devstructure.com/working_remotely> for more options.

doubledown-fsevents(1) watches a directory and relays changes.  It is called by `doubledown`.