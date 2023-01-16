# Debian-based Dockerfile notes

## Image source
From Docker hub official Debian image page: https://hub.docker.com/_/debian

Chose `bookworm-slim` in order to
* use the most current packages
* be as small as possible

Debian bookworm packages: https://packages.debian.org/bookworm/

Downside - the image is still quite large, around 850 MB

## commands
### `apt-get update`
To fetch the package lists from the Sources so that it knows what packages are available

https://www.debian.org/doc/manuals/apt-guide/ch2.en.html

https://manpages.debian.org/jessie/apt/apt-get.8.en.html

### `apt-get -y install`
To install packages by name

https://www.debian.org/doc/manuals/apt-guide/ch2.en.html

https://manpages.debian.org/jessie/apt/apt-get.8.en.html

* `-y` - assume "yes" as answer to all prompts and run non-interactively, otherwise the image build errors out

### `wget`
Required to subsequently download the IG Publisher

### `curl`
Required by the IG publisher scripts

### `ruby-full`
Ruby installation for the IG publisher to complete the build

### `build-essential`
Required to build the jekyll gem

See install jekyll on Debian instructions: https://jekyllrb.com/docs/installation/other-linux/#debian

### `git`
Required by the IG Publisher build process as well as updating the IG Publisher scripts submodule

### `openjdk-17-jre-headless`
Java runtime environment for the IG publisher jar

See java package options here: https://packages.debian.org/bookworm/java/

### `gem install jekyll --no-document`
Installs the jekyll gem without documentation