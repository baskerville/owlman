![owl](https://github.com/baskerville/owl/raw/master/preview/owl_logo.jpg)

## Description

`owl` is a `pacman` and `cower` wrapper focused on simplicity.

## Usage

    SYNOPSIS
        owl <ACTION> [OPTIONS] [ARGUMENTS]

    ACTIONS
        update
            Update package list and upgrade all packages afterwards.

        pull
            Grab changes for all the cached AUR packages.

        install PKG ...
            Install the given packages.

        remove PKG ...
            Remove the given packages.

        download PKG ...
            Download the given packages from the AUR.

        info PKG ...
            Retreive informations on the given packages.

        deps PKG ...
            Show dependencies for the given packages.

        uses PKG ...
            Show packages that specify the given packages as dependency.

        page PKG ...
            Opens the given packages AUR pages.

        home PKG ...
            Opens the given packages home pages.

        search STRING
            Search for packages matching STRING in all databases.

        query STRING
            Search locally for packages matching STRING.

        list PKG ...
            List all the files owned by the given packages.

        lsgrep STRING PKG ...
            Restrict the output of 'list' to packages matching STRING.

        binlist PKG ...
            Restrict the output of 'list' to executable files.

        etclist PKG ...
            Restrict the output of 'list' to configuration files.

        manlist PKG ...
            Restrict the output of 'list' to manual files.

        doclist PKG ...
            Restrict the output of 'list' to documentation files.

        grep STRING PKG ...
            Grep STRING in all the files of all the given packages.

        version PKG ...
            Return the version of the given packages.

        repository PKG ...
            Return the repository of the given packages.

        description PKG ...
            Return the description of the given packages.

        category PKG ...
            Return the category of the given AUR packages.

        owns FILE
            Return the name of the package owning the given file.

        cleanup
            Remove unused repositories in the cache directory.

        leftovers
            Search and propose merges for 'pac{new,orig,save}' files.

        foreigns
            Show installed packages not found in the sync databases.

        orphans
            Show packages not listed as a dependency by any package.

## Options

- **-a, --aur** -- restrain the action to the AUR packages.

- **-o, --repo** -- restrain the action to the sync packages.

- **-l, --local** -- restrain the action to the local packages.

- **-i, --ignore-outdated** -- exclude outdated AUR packages from search results.

- **-s, --recursive** -- see pacman's remove options.

- **-c, --cascade** -- see pacman's remove options.

- **-d, --dependencies** -- fetch dependencies.

- **-w, --crawl-homes** -- open every pages of all the packages matching the argument.

## Configuration

The following environment variables are handled:

- **XDG_AUR_HOME** -- where should the downloaded AUR packages be stored?

- **BROWSER** -- the browser used for opening the package's home pages.

- **OWL_SUDO_WARN** -- print a warning each time sudo is run (default value: 'true').

- **OWL_COLOR_RESULTS** -- colorize search results (default value: 'true').

- **OWL_IGNORE_OUTDATED** -- wether to ignore outdated AUR results (default value: 'false').

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
