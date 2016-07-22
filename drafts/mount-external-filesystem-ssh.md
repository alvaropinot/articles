# Mount a external filesystem over SSH on Mac

## Install

Install homebrew if you don't have it already (more info at http://brew.sh):

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Install osxfuse:

```
$ brew cask install osxfuse
```

Install sshfs:

```
$ brew install sshfs
```


## Make mounting points

Make a folder for the remotes mounts locations, called for example `remotes`.

```
$ mkdir ~/remotes
```

Make a folder for each remote you want to mount. I'll be mounting a raspberry pi
in this example, so I'm making a `rpi` folder, but you can give it any name you
want.

```
$ cd ~/remotes
$ mkdir rpi
```

Repeat this last step for every remote machine you will want to mount.


## Mount
Mount the remote directory with `sshfs`:

```
$ sshfs <remote-user>@<ip | hostname>:/ ~/remotes/<remote>
```

for example, as my raspberry pi IP is `192.168.1.7` and I'm using the default
user `pi` the command would look like:

```
$ sshfs pi@192.168.1.7:/ ~/remotes/rpi
```

Now you can `cd` into your remote folder and work with your files as they where
local 😎

```
$ cd ~/remotes/rpi
```

For example a simple `ls` at `~/remotes/rpi` would print something like

```
bin        home       mnt        run        tmp
boot       lib        opt        sbin       usr
dev        lost+found proc       srv        var
etc        media      root       sys
```

You may start developing in that same folder just by opening your editor, for
exmample Atom:

```
$ atom .
```
