# Pre-commit-hooks Collections

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

## Motivation

To facilitate starting a new project, I started to gather all the pre-commit yaml that the project will use

## Introduction of pre-commit

> Git hook scripts are useful for identifying simple issues before submission to code review. We run our hooks on every commit to automatically point out issues in code such as missing semicolons, trailing whitespace, and debug statements. By pointing these issues out before code review, this allows a code reviewer to focus on the architecture of a change while not wasting time with trivial style nitpicks.
>
> Ref: https://pre-commit.com

**TL;DR**: when developing collaboratively, we typically use git for version control and commit any changes to a feature branch that is reviewed before merging into the main codebase.

The problem is - **nothing stops us from committing low-quality code to the git repository.**

So to improve our code quality and unify the layout, styles etc, `pre-commit` hook is here to help

## Installation

- Using pip:

    ```bash
    $ pip install pre-commit
    ```

- MacOS: [homebrew](https://brew.sh/)

    ```bash
    brew install pre-commit
    ```

- Conda:

    ```bash
    conda install -c conda-forge pre-commit
    ```

## Setup & Configs

### Local

You can simple copy paste one of the example in the collection folders, or run

```bash
$ pre-commit sample-config
```

to generate a basic config.

Then you will need to install it

```bash
$ pre-commit install
```

To verify the commit message, you will need to also install

```bash
$ pre-commit install --hook-type commit-msg
```

For morte configureation, please check https://pre-commit.com/#pre-commit-configyaml---top-level



### CI/CD

To use it in CI: https://pre-commit.com/#usage-in-continuous-integration

Also, in some ci/cd services, there's already some "stage" avaiable

- Pre-commit.ci: https://pre-commit.ci

- Github: https://github.com/pre-commit/action

- Gitlab: https://gitlab.com/gitlab-org/gitlab/-/tree/master/lib/gitlab/ci/templates

- Bitbucket: https://confluence.atlassian.com/bitbucketserver/using-repository-hooks-776639836.html

- Jenkins: https://www.jenkins.io/doc/book/managing/groovy-hook-scripts/
