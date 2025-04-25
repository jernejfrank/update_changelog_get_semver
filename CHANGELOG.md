# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Removed (major)

### Changed - breaking (major)

### Added (minor)

### Changed - backward compatible (minor)

### Deprecated (minor)

### Fixed (patch)

### Security (patch)



## [1.0.0] - 25-04-2025

### Removed (major)
- migrated to public personal repo for now to have universal access



## [0.3.0] - 24-04-2025

### Changed - backward compatible (minor)
- Updated readme to reflect usage



## [0.2.0] - 24-04-2025

### Added (minor)
- add github action to parse changelog of this repo
- add release notes into the env variable to access it elsewhere



## [0.1.1] - 24-04-2025

### Fixed (patch)
- defaults to version 0.0.0 in case no changelog history


## [0.1.0] - 24-04-2025

### Added (minor)
- CHANGELOG_TEMPLATE.md to have always the same unreleased section at the top
- action.yaml for copying changelog into action repo, parsing it, and copying back
- parse_changelog.sh to extract latest version from changelog, bumping to new version
and outputting it as github env variable

