![owl](http://f.cl.ly/items/0G0U0U3E0q1r2t140g0h/owl.jpg)

## Description

`owl` is a `pacman` and `cower` wrapper focused on simplicity.

## Usage

    SYNOPSIS
        owl <action> [arguments]

    ACTIONS
        update
            Update package list and upgrade all packages afterwards.
        add PKG ...
            Install the given packages.
        remove PKG ...
            Remove the given packages.
        download PKG ...
            Download the given packages from the AUR.
        info PKG ...
            Retreive informations on the given packages.
        page PKG ...
            Opens the given packages AUR pages.
        home PKG ...
            Opens the given packages home pages.
        find STRING
            Search for packages matching STRING in the sync databases.
        search STRING
            Search for packages matching STRING in the AUR.
        query STRING
            Search locally for packages matching STRING.
        list PKG ...
            List all the files owned by the given packages.
        bin PKG ...
            Restrict output of 'list' to executable files.
        etc PKG ...
            Restrict output of 'list' to configuration files
        man PKG ...
            Restrict output of 'list' to manual files.
        grep STRING PKG ...
            Search for STRING in all the files belonging to the given packages.
        owner FILE
            Return the name of the package owning the given file.
        leftovers
            Search and propose merges for 'pac{new,orig,save}' files.
        foreigns
            Show installed packages not found in the sync databases.
        orphans
            Show packages not listed as a dependency by any package.

## Abbreviations

Most of the actions have an equivalent one letter form which always corresponds
to the first letter of the full form.

Some actions also feature an uppercase one letter form:

- `R`: also remove installed dependencies.

- `S`: also searches among official repositories.

- `F`: also searches among the AUR if no packages match in the official repositories.

- `D`: downloads even if the download directory already exists.

- `H string`: opens every home pages from the results of a `search` action on the given *string*.

- `L string pkg ...`: filter results of the `list` action with *string*.

- `U`: looks for AUR updates.

Actions without a one letter form: `leftovers`, `foreigns` and `orphans`.

## Configuration

The following environment variables should be set by the user (preferably in .bash_profile or something similar):

- **XDG_AUR_HOME** -- where should the downloaded AUR packages be stored?

- **BROWSER** -- the browser used for opening the package's home pages.

- **OWL_MAX_URL** -- the maximum number of URL this program is allowed to send to
  the BROWSER in one go.
