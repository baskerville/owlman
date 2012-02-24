![owl](https://github.com/baskerville/owl/raw/master/preview/owl_logo.jpg)

## Description

`owl` is a `pacman` and `cower` wrapper focused on simplicity.

## Usage

    SYNOPSIS
        owl <action> [arguments]

    ACTIONS
        update
            Update package list and upgrade all packages afterwards.

        checkout
            Grab changes for all the cached AUR packages.

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
            Restrict the output of 'list' to executable files.

        etc PKG ...
            Restrict the output of 'list' to configuration files.

        man PKG ...
            Restrict the output of 'list' to manual files.

        grep STRING PKG ...
            Search for STRING in all the files belonging to the given packages.

        owner FILE
            Return the name of the package owning the given file.

        clean
            Remove unused repositories in the cache directory.

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

- `D`: downloads even if the download directory already exists.

- `H string`: opens every home pages from the results of a `search` action on the given *string*.

- `L string pkg ...`: filter results of the `list` action with *string*.

- `U`: looks for AUR updates.

- `Q | F | S`: be quiet.

Actions without a one letter form: `clean`, `leftovers`, `foreigns` and `orphans`.

## Configuration

The following environment variables are handled:

- **XDG_AUR_HOME** -- where should the downloaded AUR packages be stored?

- **BROWSER** -- the browser used for opening the package's home pages.

- **OWL_SUDO_WARN** -- print a warning each time sudo is run (default value: 'true').

- **OWL_COLOR_RESULTS** -- colorize search results (default value: 'true').

- **OWL_MAX_URL** -- the maximum number of URL this program is allowed to send to
  the BROWSER in one go.

Color related variables (self-explained):

- **OWL_LOCAL_COLOR**

- **OWL_CORE_COLOR**

- **OWL_EXTRA_COLOR**

- **OWL_COMMUNITY_COLOR**

- **OWL_TESTING_COLOR**

- **OWL_AUR_COLOR**

- **OWL_SEP_COLOR**

- **OWL_NAME_COLOR**

- **OWL_VERSION_COLOR**

- **OWL_OBSOLETE_COLOR**

- **OWL_INSTALLED_COLOR**

The valid values for the aforementioned variables are : black, red, green, yellow, blue, magenta, cyan, white, bold.

## Dependencies

`sudo`, `dash` (or any POSIX shell), `cower`, `pacman` and `bash` (for package name completion).
