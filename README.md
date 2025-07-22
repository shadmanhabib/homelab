# Homelab
Documentation outlining the homelab architecture. You can find the full site at [docs.shadmanhabib.com](http://docs.shadmanhabib.com).

## Table of Contents
- [Network-Docs](#network-docs)
  - [Table of Contents](#table-of-contents)
  - [About The Project](#about-the-project)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Build](#build)
    - [Deploy](#deploy)
  - [Usage](#usage)
  - [Changelog](#changelog)

## About The Project


## Getting Started
To rebuild or update this project, the following steps may be followed.

### Prerequisites
- Python 3.11 as required by MkDocs
- An installation of MkDocs, specifically Material for MkDocs.

### Build
- Serve live updates for testing and development with `mkdocs serve` and available at [localhost:8000](http://127.0.0.1:800).
- Build deployable site with `mkdocs build` which will create a new `site` directory with all the required HTML files and assets.

### Deploy
- Copy the contents of the `site` directory to the directory of the web server to deploy.
- The following command can be run in the web server directory to fetch all files. 

```
Gotta work out how to do this.
```

## Usage
Once deployed, the full site will be available to any device on the home network or through a VPN at [network-pi.home](http://network-pi.home). The site can be used as a reference source for future installations, updates and maintenance.

## Changelog
All notable changes to this project will be documented in this section.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project attempts to adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

### [v0.0.0]
#### Initial dev
- Initiated Git repo.
- Commited first draft structure of site.