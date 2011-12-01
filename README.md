# owl -- a dash pacman / cower wrapper

![owl](http://f.cl.ly/items/0G0U0U3E0q1r2t140g0h/owl.jpg)

## Usage

    SYNOPSIS
        owl <action> [arguments]

    ACTIONS
        update
            Update the system.
        add pkg1 [pkg2 ...]
            Install the packages.
        remove pkg1 [pkg2 ...]
            Remove the packages.
        download pkg1 [pkg2 ...]
            Download the packages from the aur.
        info pkg1 [pkg2 ...]
            Retreive informations on the packages.
        page pkg
            Opens the package's aur page.
        home pkg1 [pkg2 ...]
            Opens the packages home pages.
        find string
            Search for packages matching 'string' in the official repos.
        search string
            Search for packages matching 'string' in the aur.
        query string
            Search locally for packages matching 'string'.
        list pkg1 [pkg2 ...]
            List the files owned by the given packages.
        bin pkg1 [pkg2 ...]
            Filter binaries form the 'list' action.
        etc pkg1 [pkg2 ...]
            Filter config files from the 'list' action.
        man pkg1 [pkg2 ...]
            Filter manuals from the 'list' action.
        grep string pkg1 [pkg2 ...]
            Search for 'string' in all the files belonging to the packages..
        owner file
            Return the name of the package owning the given file.
        leftovers
            Search and propose merges for pac{new,orig,save} files.
        foreigns
            Show manually installed packages.
        orphans
            Show packages not listed as a dependency by any package.

## Abbreviations

Most of the actions have an equivalent one letter long form which generally
corresponds to the first letter of the long form. Some actions also feature an
uppercase one letter form which meaning differs from its lowercase and long
counterparts by doing more of the same thing.

Actions providing an uppercase one letter form:

- `remove`: also remove installed dependencies.

- `search`: also searches among official repositories

- `find`: also searches among the AUR if no packages match in the official repositories.

- `download`: downloads even if download directory already exists.

- `home`: opens every home pages from the results of a `search` action on the given string.

- `list`: filter files based on the first argument.

- `update`: also checks for AUR updates.

Actions without a one letter form: `leftovers`, `foreigns` and `orphans`.

## Configuration

The following environment variables should be set by the user (preferably in .bash_profile or something similar):

- XDG_AUR_HOME -- where should the downloaded AUR packages be stored?

- BROWSER -- the browser used for opening the package's home pages.

- OWL_MAX_URL -- the maximum number of URL this program is allowed to send to
  the BROWSER in one go.
