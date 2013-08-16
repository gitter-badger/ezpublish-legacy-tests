# eZ Publish Legacy Tests

Execute PHPUnit tests for eZ Publish Legacy, optionally with one or more activated
extensions.

## Testable extensions

- ezformtoken (included in eZ Publish LS)
- ezjscore (included in eZ Publish LS)
- ezoe (included in eZ Publish LS)
- ezcomments
- ezprestapiprovider

## Requirements

### Phing

```
pear channel-discover pear.phing.info
pear install phing/phing
```

### PEAR/VersionControl_Git

```
pear install VersionControl_Git-0.4.4
```

### MySQL and a test database

Out of the box, the script expects a MySQL server instance at `127.0.0.1`, a database named `ezpublish_test`,
and user `root` with no password. If you want to override those values, copy the file `config/config.properties` to
`config/config_local.properties` and change the variables.


## Installation

Clone this repository

```
git clone https://github.com/jeromegamez/ezpublish-legacy-tests.git
```

## Usage

### eZ Publish Legacy standalone

```
phing test
```

### eZ Publish Legacy with one extension

```
phing test -Dextensions=ezprestapiprovider
```

### eZ Publish Legacy with multiple extensions

```
phing test -Dextensions=ezprestapiprovider,ezcomments
```
