# owl -- a dash pacman / cower wrapper

## Usage

    usage: owl <action> [arguments]
    where <action> is one of:
        update -- update the system
        info pkg1 [pkg2 ...] -- retreive informations on the packages
        query string -- search locally for packages matching string
        find string -- search for the given package in the official repos and fallback to aur
        search string -- search for the given package in both the official repos and the aur
        list pkg1 [pkg2 ...] -- list the files belonging to the packages
        owner file -- return the name of the package owning the given file
        download pkg1 [pkg2 ...] -- download the packages from the aur
        remove pkg1 [pkg2 ...] -- remove the packages
        add pkg1 [pkg2 ...] -- install the packages
        home pkg1 [pkg2 ...] -- opens the packages home pages
        bin pkg1 [pkg2 ...] -- filter binaries form the 'list' action
        etc pkg1 [pkg2 ...] -- filter config files from the 'list' action 
        man pkg1 [pkg2 ...] -- filter manuals from the 'list' action
        leftovers -- search and propose merges for pac{new,orig,save} files
        foreign -- show manually installed packages
        orphan -- show packages not listed as a dependency by any package

## Abbreviations

Most of the actions have an equivalent one letter long form which generally
corresponds to the first letter of the long form. Some actions also feature an
uppercase one letter form which meaning differs from its lowercase and long
counterparts by doing more of the same thing.

Actions providing an uppercase one letter form: *remove* (also remove installed
dependencies), *home* (opens every home pages from the results of a *search*
action on the given string) and *update* (also checks for AUR updates).

Actions without a one letter form: *leftovers*, *foreign* and *orphan*.

## Configuration

The following environment variables should be set by the user (preferably in .bash_profile or something similar):

- XDG_AUR_HOME -- where should the downloaded AUR packages be stored?

- BROWSER -- the browser used for opening the package's home pages.

- OWL_MAX_URL -- the maximum number of URL this program is allowed to send to
  the BROWSER in one go.
