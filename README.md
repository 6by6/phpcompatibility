# sixbysix/phpcompatibility

## Overview

This image bundles together the `phpcs` analysis tool with the `PHPCompatiblity` standard. 

See:
- https://github.com/squizlabs/PHP_CodeSniffer
- https://github.com/PHPCompatibility/PHPCompatibility

## Usage

```
docker run -v $PWD:/src sixbysix/phpcompatibility phpcs .
```

The above will scan the current directory for PHP compatibility issues with the following
configuration options:
- `colors` on
- `standard` PHPCompatibility

You may pass in any additional options as required (https://github.com/squizlabs/PHP_CodeSniffer/wiki/Usage), for example
if you were analysing a Magento 1 codebase you may wish to only look for incompatibilities within
the local codepool:

```
docker run -v $PWD:/src sixbysix/phpcompatibility phpcs app/code/local
```

