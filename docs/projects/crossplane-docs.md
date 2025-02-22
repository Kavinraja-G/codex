---
comments: false
---
## What is XDocs?
- We have XR, XRD, XRC ;) Why not XDocs?
- Inspired from [terraform-docs](https://github.com/terraform-docs/terraform-docs) but for [Crossplane](https://www.crossplane.io/)
- Generate markdown based docs for your Compositions, it also includes your linked Resources, XRD and Claim

## Installation
**XDocs** Generator can be installed in several ways to suit your preferences and development environments
### Homebrew Tap (macOS & Linux)

If you're using Homebrew, you can install the tool via our custom Homebrew tap

``` sh
brew tap Kavinraja-G/tap
brew install crossplane-docs
```
### Standalone Binary
For macOS, Linux, and Windows, standalone binaries are available. Download the appropriate binary for your operating system from the [releases](https://github.com/Kavinraja-G/crossplane-docs/releases/) page, then move it to a directory in your PATH.

#### macOS/Linux
``` sh
# Feel free to change the release/arch names accordingly
curl -Lo crossplane-docs https://github.com/Kavinraja-G/crossplane-docs/releases/download/v0.1.2/crossplane-docs_v0.1.2_darwin_amd64.tar.gz
chmod +x crossplane-docs
sudo mv crossplane-docs /usr/local/bin/
```
#### Windows
Download the `.exe` file and add it to your `PATH`

## Usage
Currently xDocs supports only markdown output, but more in pipeline. To generate markdown docs for your compositions & XRDs
``` sh
crossplane-docs md [INPUT_PATH|INPUT_FILE] -o [OUTPUT_FILE]
```
For example:
``` sh
crossplane-docs md ./samples -o samples/README.md
```
Check [README.md](https://github.com/Kavinraja-G/crossplane-docs/blob/main/samples/README.md) for the output.

## Features
- Discovers Composition & its resources, XR, XRD and Claim names with their references
- Markdown ouput with tabulation
- Claim/XRC specifications (WIP)

## Limitations
Crossplane compositions with Pipeline composition mode is not supported.