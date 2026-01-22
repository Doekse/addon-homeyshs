# Changelog

All notable changes to this add-on will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [12.11.1] - 2026-01-22
### Changed
- Updated Homey Self-Hosted Server base image to version 12.11.1
- You can check out the Homey Self-Hosted Server changelog here: https://homey.app/en-us/wiki/homey-shs-changelog/

## [0.0.5] - 2025-01-27

### Fixed

- Fixed rrdcached service crash (exit code 5) by implementing a wrapper script that handles path resolution issues
- Fixed persistent storage setup by switching from cont-init.d approach to entrypoint wrapper (base image doesn't use s6-overlay)
- Fixed license shield link in README

### Changed

- Refactored Dockerfile to use rootfs directory structure instead of copying individual files
- Changed privileged mode configuration from specific capabilities to `full_access: true` for better compatibility
- Simplified persistent storage setup to use symlinks instead of bind mounts for better reliability
- Improved code comments throughout the codebase
- Updated port numbers in documentation and configuration to correct values (HTTP: 4859, HTTPS: 4860, Bridge V2: 4862)

### Added

- Added webui and watchdog configuration in config.yaml
- Added Web UI documentation section
- Added build.yaml for custom base image support
- Added rrdcached wrapper script to handle path resolution issues
- Added entrypoint wrapper script for persistent storage configuration

## [0.0.4] - 2025-01-27

### Added

- Added troubleshooting note in documentation for when Home Assistant can't find the add-on after adding the repository

### Fixed

- Fixed license link path in README
- Fixed documentation link formatting

### Changed

- Reordered support section in main README for better organization

## [0.0.3] - 2025-12-16

### Fixed

- Fixed image path encoding in README (space to URL encoding)
- Improved documentation formatting in support section

## [0.0.2] - 2025-12-16

### Changed

- Updated repository URLs to `addon-homeyshs` across all documentation and configuration files

### Added

- Added image to README files

## [0.0.1] - 2025-12-16

### Added

- Initial release of Homey Self-Hosted Server add-on
- Support for amd64 and aarch64 architectures
- Host networking support for device discovery
- Automatic data persistence

