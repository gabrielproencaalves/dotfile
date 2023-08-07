# dotfile

Automated dotfiles installation script.

# How to install

1. Download it via [zip file](https://thelinkofthefile/) or git:

`$ clone https://github.com/gabrielproencaalves/dotfile.git`

And that's it. As an interpreted shell file, the dotfile script does not require other software, besides a shell interpreter and a text editor, to be used.

# How to use

Basically, this program is composed of three parts:

- _dotfile_: The script itself.

- _index_: The list of paths of
files and folders tracked by
dotfile (the paths are
relative to user home).

- _db_: The directory that holds
the copies of listed files and
folders from index.


Dotfile can do two operations:

- _sync_: Run through index and
asks which file needs to be
replaced in db.

- _setup_: Copies each file/folder
from db to actual user home.


Here is an example:

index content:

```none
  .bashrc
  .nanorc
  .profile
```

Then, if user executes:

`$ ./dotfile sync`

dotfile checks if the three index files
are already stored in db, if they aren't,
just copies them to db, else, asks to
replace existing db files.

Another example is:

index content:

```none
  .bashrc
  .nanorc
  .profile
```

With that, if the user runs:

`$ ./dotfile setup`

dotfile installs each file from db/index into
the home of actual user.
