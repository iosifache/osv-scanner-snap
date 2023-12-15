<p align="center">
    <a href="https://google.github.io/osv-scanner/">
        <img src="images/logo.png" height="100" alt="OSV-Scanner logo"/>
    </a>
</p>
<h2 align="center">Vulnerability scanner for project's dependencies</h2>
<p align="center" float="left">
    <a href="https://snapcraft.io/osv-scanner">
        <img src="https://snapcraft.io/osv-scanner/badge.svg" width="150" height="17" alt="Snapcraft's Version"/>
    </a>
    &nbsp; &nbsp;
    <a href="https://snapcraft.io/osv-scanner">
        <img src="https://img.shields.io/github/v/release/google/osv-scanner?label=OSV-Scanner%20on%20GitHub%20Releases&color=1c8223" height="17" alt="PyPI's Version">
    </a>
    &nbsp; &nbsp;
    <a href="https://github.com/iosifache/osv-scanner-snap/actions/workflows/test-build.yaml">
        <img src="https://img.shields.io/github/actions/workflow/status/iosifache/osv-scanner-snap/test-build.yaml?label=Build%20Status&color=1c8223" height="17" alt="GitHub Build Workflow Status">
    </a>
</p>

# Description

OSV-Scanner is a vulnerability scanner that examines your project's list of dependencies and reports any vulnerabilities that affect the versions you're using. The goal of this repository is to package OSV-Scanner as a (community) snap that can be effortlessly installed across a variety of Linux distributions.

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/osv-scanner)

> Notice: If you want to view the officially recommended method of installing of the tool, refer to the [OSV-Scanner documentation](https://google.github.io/osv-scanner/installation/).
  
As of December 2023, it supports lockfiles from C, C++, Dart, Elixir, Go, Java, JavaScript, PHP, Python, R, Ruby, and Rust. It also supports custom lockfiles: simply write some glue code to convert your lockfile into an intermediary JSON file with a particular format, and OSV-Scanner will comprehend the latter.

After confirming that a reported vulnerability is a false positive or discovering mitigations other than upgrading the package, OSV-Scanner provides the option to suppress it so that future runs will not display it.

# Local Build

1. Clone this repository: `git clone https://github.com/iosifache/osv-scanner-snap`
2. Move into the cloned repository: `cd osv-scanner-snap`
3. Install Snapcraft: `sudo snap install snapcraft --classic`
4. Build the snap: `snapcraft --verbose`
5. Install the snap: `snap install --dangerous ./osv-scanner_*.snap`
6. Test the snap by running the `osv-scanner` command: `osv-scanner`
