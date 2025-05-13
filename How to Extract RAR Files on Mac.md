This guide explains how to extract RAR files on macOS using the Terminal.

## Installation Process

When trying to extract RAR files on Mac using the command line, you may encounter some initial challenges:

First attempt to install ```unrar```:

```
brew install unrar
```

<br> 

Result: Command not available

```
Warning: No available formula with the name "unrar". Did you mean unar?
```

<br>

Homebrew suggests alternatives:

```
==> Searching for similarly named formulae and casks...
==> Formulae
unar

To install unar, run:
  brew install unar

==> Casks
lunar

To install lunar, run:
  brew install --cask lunar
```

<br>

As shown above, ```unrar``` is not available as a Homebrew formula, but ```unar``` is recommended as an alternative.

<br>

## Installing ```unar```

Install the recommended alternative:

```
brew install unar
```

<br>

Installation output:

```
==> Downloading https://ghcr.io/v2/homebrew/core/unar/manifests/1.10.8_6
######################################################################### 100.0%
==> Fetching unar
==> Downloading https://ghcr.io/v2/homebrew/core/unar/blobs/sha256:3c3885c3e70e7
######################################################################### 100.0%
==> Pouring unar--1.10.8_6.arm64_sequoia.bottle.tar.gz
🍺  /opt/homebrew/Cellar/unar/1.10.8_6: 64 files, 13.4MB
==> Running `brew cleanup unar`...
```

<br>

## Extracting RAR Files

Once ```unar``` is installed, you can extract RAR files with a simple command:

```
unar materials.rar
```

This will extract the contents of the RAR file to the current directory.

<br>

## Additional unar Options

* Extract to a specific location: ```unar materials.rar -o /path/to/destination/```
* Extract with password: ```unar materials.rar -p "your_password"```
* List contents without extracting: ```lsar materials.rar```

