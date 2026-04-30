# Contributing

If you have an idea or feature request, please open an [issue][1] even if you do
not have time to contribute!

## Making Changes

> [!IMPORTANT]
> This guide assumes you have a functioning Python 3.12 (or later) environment
> with [uv][2] installed and available in `PATH`. On Linux, [pcsclite][3] must
> also be installed as a [dependency][4].

To get started, [fork][5] this repository on GitHub and clone a working copy for
development:

```shell
git clone git@github.com:YOUR-USERNAME/nfc-labeler.git
```

Once cloned, change the directory to your working copy and update the project
environment by issuing:

```shell
uv sync --locked
```

To run tests, issue:

```shell
uv run pytest
```

Finally, commit your changes and open a [pull request][6] against the default
branch for review. Ensure there are no test regressions, and add tests for any
new functionality.

> [!TIP]
> Code quality checks are enabled for this repository. A Git pre-commit hook is
> available to run checks automatically, which can be installed after updating
> the project environment by issuing `uv run prek install`.

## Making Releases

Making releases is automated by [GitHub Actions][7]. Releases are created from
the default branch; as such, tests should be passing at all times.

To make a release, perform the following:

1. Update the project version by issuing:

   ```shell
   uv version --bump <major|minor|patch>
   ```

1. Create a new section in the [Changelog][8] for the release using the
   [Common Changelog][9] format.

2. Commit outstanding changes by issuing:

   ```shell
   git commit -a -m "Release v<version>"
   ```

3. Push changes to the remote repository and verify the results of the [CI][10]
   workflow:

   ```shell
   git push origin <default-branch>
   ```

4. Create a release tag by issuing:

   ```shell
   git tag -a -m "Release v<version>" v<version>
   ```

5. Push the release tag to the remote repository and verify the results of the
   [Release][11] workflow:

   ```shell
   git push origin --tags
   ```

## AI Tool Use Policy

This repository adheres to the [LLVM AI Tool Use Policy][12]:

Contributors may use AI tools, but a human must be in the loop. Submissions must
be understood, reviewed, and owned by the contributor. Substantial AI-assisted
content must be attributed using a `Co-authored-by` commit trailer and disclosed
in pull request descriptions. Use of autonomous agents is not permitted.

## License

By contributing to this repository, you agree that your contributions will be
licensed under its Simplified BSD License.

[1]: https://github.com/sstallion/nfc-labeler/issues
[2]: https://docs.astral.sh/uv/getting-started/installation/
[3]: https://pcsclite.apdu.fr/
[4]: https://pyscard.sourceforge.io/user-guide.html#introduction
[5]: https://docs.github.com/en/github/getting-started-with-github/fork-a-repo
[6]: https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request
[7]: https://docs.github.com/en/actions
[8]: https://github.com/sstallion/nfc-labeler/blob/main/CHANGELOG.md
[9]: https://common-changelog.org/
[10]: https://github.com/sstallion/nfc-labeler/actions/workflows/ci.yml
[11]: https://github.com/sstallion/nfc-labeler/actions/workflows/release.yml
[12]: https://llvm.org/docs/AIToolPolicy.html
