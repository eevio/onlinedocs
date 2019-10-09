# eevio Online Documentation

This repository contains the eevio Online Documentation set. It is managed by [DocFX](https://dotnet.github.io/docfx/) with each area of documentation being represented as a git submodule pointing to another repository (_prefixed with the term 'docs'_).

To begin clone this repository using `git clone --recursive <projectUrl>`. This command will ensure that the associated submodules containing the referenced documentation is also downloaded. The `.gitmodules` file describes these referenced repositories along with the branch name that should be used when building the documentation set.

## Building the Documentation Set

Refer to the DocFX documentation to execute the build.

### Continuous Integration Builds

Cloning this repository using the `--recursive` option will be enough to initialize a build.

It is important to note that the `branch` values defined in `.gitmodules` will determine the overall set of files that will be included in the build of the documentation set.

### Desktop Builds

To keep the referenced submodules up to date with the configured branches defined in `.gitmodules`, run `git submodule update --recursive --remote` in the root of the repository. Running `docfx --serve` will then complete a desktop build.