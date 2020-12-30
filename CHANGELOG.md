# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
### Changed
- default python to 3.9.0
- simplified variable definitions
- BREAKING: uses /home/<user>/tmp by default as Python build requires executables in temp directory
- Build tooling updated (Travis, Ansible, Molecule, Goss)
- Pre-commit hooks updated

### Deprecated
### Removed
  - RedHat/CentOS 6 no longer supported
### Fixed
### Security

## [2.0.0] 2020-12-30
### Changed
- default python to 3.9.0
- simplified variable definitions
- BREAKING: uses /home/<user>/tmp by default as Python build requires executables in temp directory
- Build tooling updated (Travis, Ansible, Molecule, Goss)
- Pre-commit hooks updated
### Removed
  - RedHat/CentOS 6 no longer supported

## [1.0.2]
### Changed
- PyEnv updated to 1.2.16
- Ansible updated to 2.9.2 for support

## [1.0.1] - 2019-08-13
### Changed
- PyEnv updated to 1.2.13, PyEnv Virtual updated to 1.1.15
- Ansible updated to 2.8.3 for tests
- Molecule updates (minor)
- Pre-commit updates (minor)

## [1.0.0] - 2019-02-04
### Added
- Initial version

[Unreleased]: https://github.com/bdellegrazie/ansible-role-python_pyenv/compare/v2.0.0...HEAD
[2.0.0]: https://github.com/bdellegrazie/ansible-role-python_pyenv/compare/v1.0.2...v2.0.0
[1.0.2]: https://github.com/bdellegrazie/ansible-role-python_pyenv/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/bdellegrazie/ansible-role-python_pyenv/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/bdellegrazie/ansible-role-python_pyenv/compare/...v1.0.0
