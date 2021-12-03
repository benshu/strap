# Strap

A script to bootstrap a minimal macOS development system. Adapted for Intsights, a Rapid7 company.


## Motivation

Heavily -copied- inspired by [Strap](https://github.com/MikeMqcuaid/strap) from [GitHub](https://github.com/) with attempt to adapt to our environment and style.

## Ideals

- Aim for the broadest common ground sane defaults and requirement.
- Avoid personal taste as much as possible.
- Allow for extension with external dotfiles repository with simple hooks.
- Strengthen security
- Adhere to company policy

## Features

- Disables Java in Safari (for better security)
- Installs the Xcode Command Line Tools (for compilers and Unix tools)
- Agree to the Xcode license (for using compilers without prompts)
- Installs [Homebrew](https://brew.sh) (for installing command-line software)
- Installs [Homebrew Bundle](https://github.com/Homebrew/homebrew-bundle) (for `bundler`-like `Brewfile` support)
- Installs [Homebrew Services](https://github.com/Homebrew/homebrew-services) (for managing Homebrew-installed services)
- Installs [Homebrew Cask](https://github.com/Homebrew/homebrew-cask) (for installing graphical software)
- Installs the latest macOS software updates (for better security)
- Installs dotfiles from a user's `https://github.com/username/dotfiles` repository. If they exist and are executable: runs `script/setup` to configure the dotfiles and `script/strap-after-setup` after setting up everything else.
- Installs software from a user's `Brewfile` in their `https://github.com/username/homebrew-brewfile` repository or `.Brewfile` in their home directory.
- Idempotent

## Usage

To run Strap locally run:

```bash
git clone https://github.com/benshu/strap
cd strap

STRAP_GIT_NAME="VALUE" \
STRAP_GIT_EMAIL="VALUE" \
STRAP_GITHUB_USER="VALUE" \
CUSTOM_HOMEBREW_TAP="VALUE" \
CUSTOM_BREW_COMMAND="VALUE"  \
bash bin/strap.sh

# or bash bin/strap.sh --debug for more debugging output
```

## Status

Stable and in active development.

## Contact

[Hagay Ben-Shushan](mailto:hagay_benshushan@rapid7.com)

## License

Licensed under the [MIT License](https://en.wikipedia.org/wiki/MIT_License).
The full license text is available in [LICENSE.txt](https://github.com/benshu/strap/blob/master/LICENSE.txt).
