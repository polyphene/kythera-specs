# Features

In this section we will try to cover the features we are planing on delivering with the first version of Kythera. To make 
it as explicit as possible we will do so by covering the different command we plan on incorporating in our CLI.

## Global command

### `init`

**Usage**
```shell
kythera init <path> [--template <github-profile>/<github-repository>]
```

**Description**
Initialize a new Kythera project at a given path on the file system.

**Parameters**
- `path`: Path on the file system where the Kythera project will be initialized.
- `template`: If a template is specified, clone the given github repository at the given path.

### `help`

**Usage**
```shell
kythera help [<command>]
```

**Description**
Prints the available subcommands and concepts.  

**Parameters**
- `command`: Prints a specific subcommand concept and help

## Testing commands

### `test`
**Usage**
```shell
kythera test 
```

### `snapshot`

**Usage**
```shell
kythera snapshot [--diff <path>] [--check <path>] [--snap <filename>]
```

**Description**
Generates a report containing gas consumption information for the test written.

**Parameters**
- `diff`: Path to another snapshot to compare against and display changes from the snapshot. 
- `check`: Path to another snapshot to compare against and display all the differences, if any.
- `snap`: If not specified, default filename for the snapshot is `.gas-snapshot`. If specified, the snapshot is saved under
the given filename.