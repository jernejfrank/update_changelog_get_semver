# update_changelog_get_semver
Github action to parse our CHANGELOG and extract the correct version bump.

This GitHub Action automates version bumping based on the `CHANGELOG.md`.
It updates the `CHANGELOG.md` file and outputs the correct version bump to update your
project with, ensuring a structured release process.

## 🚀 Features
- 📜 **Extracts the next version** from `CHANGELOG.md`.
- 📄 **Prepares release notes** that can be added to release action.

---

## 📦 **Usage**
Add the following workflow to your `.github/workflows`:

```yaml
- name: Update Changelog and Python Package
uses: SafeIntelligence/update_changelog_get_semver@main

- name: Show new version and release notes
run: |
    echo "${{ env.new_version }}"
    echo "${{ env.release_notes }}"
```

This will then automatically parse the CHANGELOG and return the correct version bump
as the env variable ``new_version`` and latest release notes as the env variable ``release_notes``.

## 📌 Outputs

`new_version`: The bumped version number stored in `${{ env.new_version }}` for easy access by other actions.

`release_notes`: Only the just released section of the changelog.

## 📜 CHANGELOG Template

The action uses a template to structure your CHANGELOG.md.
You can customize it in your repository or use the default. The script searches for the keywords:
`major`.`minor`.`patch` to extract the correct version bump according to [semantic versioning](https://semver.org).

```
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

```

## 📄 License

MIT License © 2024 Jernej Frank
