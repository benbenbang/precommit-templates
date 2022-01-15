# pre-commit-hooks

In the `.pre-commit-hooks.yaml`, there's some out-of-the-box hooks for the pre-commit

One can add it in this section:

```yaml
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.1.0  # Use the ref you want to point at
    hooks:
    -   id: trailing-whitespace
    # -   id: ...
```

For full collections & its args, please check: https://github.com/pre-commit/pre-commit-hooks

## Some common used hooks

###### trailing-whitespace

Trims trailing whitespace.

###### check-added-large-files

Prevent giant files from being committed.

######check-ast

Simply check whether files parse as valid python.

###### check-builtin-literals

Require literal syntax when initializing empty or zero Python builtin types.

###### check-case-conflict

Check for files with names that would conflict on a case-insensitive filesystem like MacOS HFS+ or Windows FAT.

###### check-toml

Attempts to load all TOML files to verify syntax.

####### check-merge-conflict

Check for files that contain merge conflict strings.

###### check-shebang-scripts-are-executable

Checks that scripts with shebangs are executable.

###### check-xml

Attempts to load all xml files to verify syntax.

###### check-yaml

Attempts to load all yaml files to verify syntax.

###### detect-aws-credentials

Checks for the existence of AWS secrets that you have set up with the AWS CLI. The following arguments are available:

###### detect-private-key

Checks for the existence of private keys.
