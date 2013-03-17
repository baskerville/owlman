![owl](https://github.com/baskerville/owl/raw/master/logo/owl-logo.jpg)

## Description

`owl` is a `pacman` and `cower` wrapper focused on simplicity.

## Synopsis

    owl ACTION [OPTIONS] [ARGUMENTS]

## Actions and Arguments

- `refresh` — Update package list.

- `update` — Update package list and upgrade all packages afterwards.

- `pull` — Grab changes for all the cached AUR packages.

- `install PKG ...` — Install the given packages.

- `upgrade PKG ...` — Upgrade the given packages.

- `downgrade PKG ...` — Downgrade the given packages.

- `remove|uninstall PKG ...` — Remove the given packages.

- `download PKG ...` — Download the given packages source from the AUR.

- `abs PKG ...` — Download the given sync packages source via `abs`.

- `edit PKG` — Edit the PKGBUILD for the given AUR package.

- `search STRING` — Search for packages matching `STRING` in all databases.

- `query STRING` — Search locally for packages matching `STRING`.

- `info PKG ...` — Retrieve informations on the given packages.

- `deps PKG ...` — Show dependencies for the given packages.

- `mdeps PKG ...` — Show make dependencies for the given packages.

- `uses PKG ...` — Show packages that specify the given packages as dependency.

- `owns FILE` — Return the name of the package owning the given file.

- `version PKG ...` — Return the version of the given packages.

- `repository PKG ...` — Return the repository of the given packages.

- `description PKG ...` — Return the description of the given packages.

- `category PKG ...` — Return the category of the given AUR packages.

- `license PKG ...` — Return the license of the given packages.

- `page PKG ...` — Opens the given packages AUR pages.

- `home PKG ...` — Opens the given packages home pages.

- `changelog PKG ...` — Opens the given packages *changelog* pages.

- `list PKG ...` — List all the files owned by the given packages.

- `lsgrep STRING PKG ...` — Restrict the output of *list* to packages matching `STRING`.

- `binlist PKG ...` — Restrict the output of *list* to executable files.

- `liblist PKG ...` — Restrict the output of *list* to library files.

- `etclist PKG ...` — Restrict the output of *list* to configuration files.

- `manlist PKG ...` — Restrict the output of *list* to manual files.

- `doclist PKG ...` — Restrict the output of *list* to documentation files.

- `grep STRING PKG ...` — Grep `STRING` in all the files of all the given packages.

- `check PKG ...` — Check that all files owned by the given packages exist.

- `prune` — Remove unused repositories in the cache directory.

- `last [NUM]` — Show the last `NUM` (7 if omitted) installed packages.

- `leftovers` — Find, merge and remove `pac{new,orig,save}` files.

- `foreigns` — Show installed packages not found in the sync databases.

- `orphans` — Show packages not listed as a dependency by any package.

## Options
The actions on which each option applies are given between parenthesis.

- `-q, --quiet` — provide quiet search results ( *search*, *query*, *foreigns*, *orphans*, *owns*, *changelog* ).

- `-e, --extended` — provide extended informations ( *info* ).

- `-a, --aur` — restrain the action to the AUR packages ( *update*, *search* ).

- `-o, --repo` — restrain the action to the sync packages ( *update*, *search* ).

- `-l, --local` — restrain the action to the local packages ( *info*, *deps*, *uses*, *version*, *repository*, *category*, *description* ).

- `-i, --ignore-outdated` — exclude outdated AUR packages from search results ( *search* ).

- `-s, --recursive` — see pacman's remove options ( *remove* ).

- `-c, --cascade` — see pacman's remove options ( *remove* ).

- `-d, --dependencies` — fetch dependencies ( *download* ).

- `-w, --crawl-homes` — open every pages of all the packages matching the argument ( *home* ).

## Configuration

The following environment variables are handled:

- `OWL_AUR_HOME` — where should the downloaded AUR packages be stored?

- `OWL_ABS_HOME` — where should the downloaded sync packages be stored?

- `OWL_CHANGELOG_DB` — path to the database of changelog URLs.

- `OWL_ABS_ROOT` — the value of the *ABSROOT* variable in `/etc/abs.conf`.

- `OWL_PACMAN_CACHE` — the value of the *CacheDir* variable in `/etc/pacman.conf`.

- `OWL_PACMAN_LOG` — the value of the *LogFile* variable in `/etc/pacman.conf`.

- `OWL_BROWSER` — the browser used for opening the package's home pages.

- `OWL_EDITOR` — the editor used for opening the package's PKGBUILDs.

- `OWL_SUDO_WARN` — print a warning each time sudo is run (default: *true*).

- `OWL_COLORIZE_RESULTS` — colorize search results (default: *true*).

- `OWL_IGNORE_OUTDATED` — whether to ignore outdated AUR results (default: *false*).

- `OWL_CLEAN_UP` — whether to pass the `-c` flag to `makepkg` (default: *false*).

- `OWL_MAX_URL` — the maximum number of URL to send at once via `--crawl-homes`.

### Color Variables

- `OWL_LOCAL_COLOR`

- `OWL_CORE_COLOR`

- `OWL_EXTRA_COLOR`

- `OWL_COMMUNITY_COLOR`

- `OWL_TESTING_COLOR`

- `OWL_AUR_COLOR`

- `OWL_OTHER_COLOR`

- `OWL_SEP_COLOR`

- `OWL_NAME_COLOR`

- `OWL_VERSION_COLOR`

- `OWL_OBSOLETE_COLOR`

- `OWL_INSTALLED_COLOR`

The valid values for the aforementioned variables are : *default*, *black*, *red*, *green*, *yellow*, *blue*, *magenta*, *cyan*, *white*, *bold*.

## Dependencies

`sudo`, `dash` (or any POSIX compliant shell), `cower`, `pacman`, `abs` and `bash` (for package name completion).
