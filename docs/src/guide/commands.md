# Commands

## Init

### Running it

```bash
manuscript init
```

Run the command from within the directory that you want to become a manuscript root.

### Flags

`--dir -d` (Specify a directory to run the command from. Defaults to the current directory.)

### Description

Initializes a directory as a manuscript root.

A manuscript root is just a directory with a `.manuscript` file and two folders: `packages` and `playgrounds`. Other than that, there is nothing particularly special about it.

Manuscript directories are independent of one another. So feel free to create multiple. Nesting them could have some odd side-effects though.

## Create

### Running it

```bash
manuscript create
```

This command must be run from inside a manuscript root.

### Flags

`--laravel -l` (Tell manuscript to create you a Laravel package, instead of the default basic one.)

`--play -p` (Run the [play](#play) command immediately after the create process is finished.)

`--dir -d` (Specify a directory to run the command from. Defaults to the current directory.)

### Description

Scaffolds a new composer package with the `create` command. Passing the `-l` or `--laravel` flag will scaffold a 
laravel package.

Laravel packages are created from a github template provided by Spatie. Manuscript uses Github’s API to create a new 
repository in your own Github account using that template, before cloning it down to your local manuscript packages folder.

Because the laravel package scaffolding relies on Github’s API, you will need to get a [Github Personal Access Token](https://github.com/settings/tokens) 
and paste it in to the manuscript command when it asks you for it.


## Play

### Running it

```bash
manuscript play
```

This command must be run from inside a package that lives inside a manuscript package directory.

### Flags

`--dir -d` (Specify a directory to run the command from. Defaults to the current directory.)

### Description

Downloads a framework “playground” inside your local manuscript playgrounds folder and install the given package 
into it.

Once you have at least one playground installed, you will be given the option to install your package into an 
existing one. The means **you could install multiple packages you are building into a single playground**. 

It sets up the playground’s composer json to use the “path” type for your local package. This in turn symlinks your 
local package into the playground’s vendor folder. So you can develop your package locally and see the changes update in the playground as you go.

## Clear Playgrounds

### Running it

```bash
manuscript clear-playgrounds
```

This command must be run from inside a manuscript root.

### Flags

`--dir -d` (Specify a directory to run the command from. Defaults to the current directory.)

### Description

Clears out the playground directory for starting fresh. This will have no effect on your packages you are working on.
**Playgrounds are free to be discarded and then rebuilt with the `play` command**.

