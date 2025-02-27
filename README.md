[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
[![#HAXTheWeb](https://img.shields.io/badge/-HAXTheWeb-999999FF?style=flat&logo=data:image/svg%2bxml;base64,PHN2ZyBpZD0iZmVhMTExZTAtMjEwZC00Y2QwLWJhMWQtZGZmOTQyODc0Njg1IiBkYXRhLW5hbWU9IkxheWVyIDEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgdmlld0JveD0iMCAwIDE4NC40IDEzNS45NyI+PGRlZnM+PHN0eWxlPi5lMWJjMjAyNS0xODAwLTRkYzItODc4NS1jNDZlZDEwM2Y0OTJ7ZmlsbDojMjMxZjIwO308L3N0eWxlPjwvZGVmcz48cGF0aCBjbGFzcz0iZTFiYzIwMjUtMTgwMC00ZGMyLTg3ODUtYzQ2ZWQxMDNmNDkyIiBkPSJNNzguMDcsODMuNDVWNTVIODYuMnY4LjEzaDE2LjI2djQuMDdoNC4wN1Y4My40NUg5OC40VjY3LjE5SDg2LjJWODMuNDVaIi8+PHBvbHlnb24gcG9pbnRzPSIxNTMuMTMgNjMuNyAxNTMuMTMgNTEuMzkgMTQwLjU0IDUxLjM5IDE0MC41NCAzOS4wOSAxMjcuOTUgMzkuMDkgMTI3Ljk1IDI2Ljc5IDEwMi43OCAyNi43OSAxMDIuNzggMzkuMDkgMTE1LjM2IDM5LjA5IDExNS4zNiA1MS4zOSAxMjcuOTUgNTEuMzkgMTI3Ljk1IDYzLjcgMTQwLjU0IDYzLjcgMTQwLjU0IDc2IDEyNy4zNiA3NiAxMjcuMzYgODguMyAxMTQuNzggODguMyAxMTQuNzggMTAwLjYxIDEwMi4xOSAxMDAuNjEgMTAyLjE5IDExMi45MSAxMjcuMzYgMTEyLjkxIDEyNy4zNiAxMDAuNjEgMTM5Ljk1IDEwMC42MSAxMzkuOTUgODguMyAxNTIuNTQgODguMyAxNTIuNTQgNzYgMTY1LjcyIDc2IDE2NS43MiA2My43IDE1My4xMyA2My43Ii8+PHBvbHlnb24gcG9pbnRzPSIzMy4xMyA2My43IDMzLjEzIDUxLjM5IDQ1LjcyIDUxLjM5IDQ1LjcyIDM5LjA5IDU4LjMxIDM5LjA5IDU4LjMxIDI2Ljc5IDgzLjQ4IDI2Ljc5IDgzLjQ4IDM5LjA5IDcwLjg5IDM5LjA5IDcwLjg5IDUxLjM5IDU4LjMxIDUxLjM5IDU4LjMxIDYzLjcgNDUuNzIgNjMuNyA0NS43MiA3NiA1OC44OSA3NiA1OC44OSA4OC4zIDcxLjQ4IDg4LjMgNzEuNDggMTAwLjYxIDg0LjA3IDEwMC42MSA4NC4wNyAxMTIuOTEgNTguODkgMTEyLjkxIDU4Ljg5IDEwMC42MSA0Ni4zMSAxMDAuNjEgNDYuMzEgODguMyAzMy43MiA4OC4zIDMzLjcyIDc2IDIwLjU0IDc2IDIwLjU0IDYzLjcgMzMuMTMgNjMuNyIvPjwvc3ZnPg==)](https://haxtheweb.org/)

# HAXcms
The authoring experience of HAX and the ability to make fast, static file backed websites rapidly.
Get all the details you want on [HAXTheWeb.org](https://haxtheweb.org/haxcms-1)!
HAXcms seeks to be the smallest possible back-end CMS to make HAX work and be able to build websites with it. Leveraging JSON Outline Schema, HAX is able to author multiple pages, which it then writes onto the file system. This way a slim server layer is just for basic authentication, knowing how to save files, and placing them in version control.

## Features
- All the UX of HAX brought to a small CMS
- Incredibly simple, readable file structure of flat HTML files and lightning fast, high scale micro-sites
- cdn friendly configuration
- 0 config, 100% offline capable, PWA generation
- clean, simple theme layer abstracted from content
- No database (simple `.json` files help manage relationships, all pages html+webcomponents)
- Files you can reach out and touch, fork, and theme with ease!
- Support for multiple sites
- automatic git repo creation and management (never touch commandline again, but dive in if you really needed)
- Built in gh-pages publishing
- Support for PHP and Express based backends

# Requirements (PHP)
- Supports PHP 7.1+
- Requires `zip`, `gd`, and `xml` modules be installed
- Apache 2.4
# Requirements (node, still in development)
```bash
cd system/backend/nodejs
yarn run dev
```

## Quick Install
```bash
$ curl -fsSL https://raw.githubusercontent.com/elmsln/HAXcms/master/scripts/haxcmsme.sh -o haxcmsme.sh && sh haxcmsme.sh
```
## Installation Guides
- There are full installation instructions available at https://haxtheweb.org/installation which details many different install routines.
### Containers
- Clone this repo: `git clone https://github.com/elmsln/haxcms.git`
- Install a server container (recomnended). Here are some options (We support 'em all!):  
  - [docker](https://store.docker.com/search?type=edition&offering=community)
  - [ddev](https://ddev.readthedocs.io/en/latest/#installation)
  - [docksal](https://docksal.io/installation/)
  - [lando](https://docs.devwithlando.io/installation/installing.html)
  - [vagrant](https://www.vagrantup.com/downloads.html)
- Open a terminal window, go to the directory where you downloaded your container app and type `ddev start` (for ddev) or `fin init` (for docksal) or `lando start && lando magic` (for lando) or `vagrant up` (for vagrant).
- Go to the link any of them give you in a browser.
- Username/password is `admin`/`admin` to get building out static sites locally that you can push up anywhere!
- Click the icon in the top-right and you're off and running!
### MAMP
- Download [MAMP](https://www.mamp.info/)
- Download this repo https://github.com/elmsln/HAXcms/archive/master.zip
- Place HAXcms files in the htdocs folder of MAMP.
- Turn MAMP on and click "My website"
- Copy the password it gives you, click to access HAX and then HAX YOUR WEB!
## Scope
Generate `.html` files which have only "content" in them. Meaning the contents of the page in question. A simple method of adding new pages and managing the organization of those pages into a simple hierarchy (outline). Support for multiple mini web sites so that you can write a lot about different topics. HAXcms is only intended to be a micro-site generator and play nicely with the rest of the HAX ecosystem without needing a monster CMS in order to utilize it.

## Usage
Go to `yoursite.com` and login with the username and password you entered in the `_config/config.php` by clicking on the login icon

## HAXiam deployment
[HAXiam](https://github.com/elmsln/HAXiam) (HAX, I am) is a SaaS configuration for HAXcms.
It allows for the replication of HAXcms per user account for enterprise deployments. It's 
able to better interface with enterprise login systems while maintaining a clean copy of HAXcms.

HAXcms does not require HAXiam to operate but it is an alternate configuration that we support. 
Therefore if you see anything in the docs or under the hood referencing how to change settings 
when in that type of environment, you know why.

## Windows
[Cygwin command line](https://www.cygwin.com/) is lightly tested, but slower than true Bash environment.

### Windows Install
To properly configure git endlines for Windows, run this configuration
```bash
$ git config --global core.autocrlf true
```
### Fedora (31/32) Troubleshooting
Newer versions of Fedora use cgroupsv2 which is currently not supported by Docker. 
To avoid a cgroup error before running HAX locally (e.g. before using "ddev start" or "fin init") run the following commands.
```bash
sudo mkdir /sys/fs/cgroup/systemd
sudo mount -t cgroup -o none,name=systemd cgroup /sys/fs/cgroup/systemd
```
## License
[Apache 2.0](LICENSE.md)
