# LFS-qi-recipes
Qi recipes collection for Linux From Scratch.

## What's this ?

This is my personal qi recipe for Linux From Scratch. 

## How do we use those recipes for building package(s) ?

It's quite simple, for starter, make sure you have these following tools :

- `qi` & `graft`, get `qi` [here](https://dragora.mirror.garr.it/current/sources/qi-2.12.tar.lz) and graft [here](https://dragora.mirror.garr.it/current/sources/graft-2.16.tar.gz).
- `wget2` (default) or `wget`, needed for downloading source code.
- `patch`, needed for applying patch.
- archive tools, needed to unpack archive. 

If we already had those tools, it's time to build the package ! The steps it's quite simple :

1. Copy one recipe you want to use (e.g `vim.recipe`) !

    ```
    $ cp vim.recipe recipe
    ```

1. Adjust the recipe as you need !

    ```
    $ vim recipe
    ```

1. Build the package ! We can use this command :

    ```
    $ sudo qi build recipe
    ```
    
    The build process duration depends on the recipe. Just wait ! The package will be produced at /var/cache/qi/packages/amd64/ .


1. Once the package is ready, we can install it using this command :

    ```
    $ sudo qi install -p /var/cache/qi/packages/amd64/name_of_package.tlz

    ```
