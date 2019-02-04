# ansible-role-python_pyenv

Installs Python's [Pyenv](https://github.com/pyenv/pyenv) and executes an install as needed

[![Build Status](https://travis-ci.org/bdellegrazie/ansible-role-python_pyenv.svg?branch=master)](https://travis-ci.org/bdellegrazie/ansible-role-python_pyenv)

# Requirements

None

# Role Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `python_pyenv_packages`| packages to install to support pyenv, normally git and all packages needed to build python | See vars (distro specific) |
| `python_pyenv_user` | The user to install pyenv with | `root` |
| `python_pyenv_url` | Git URL to download pyenv from | `https://github.com/pyenv/pyenv.git` |
| `python_pyenv_version` | Git tag or hash of Pyenv to install | `v1.2.9` |
| `python_pyenv_user_profile` | File to put profile changes into | `.bashrc` |
| `python_pyenv_pythons_mirror_url` | URL of Pythons mirror on Github, override this for Nexus or Artifactory | `https://pyenv.github.io/pythons` |
| `python_pyenv_pythons_base_url` | URL to download Python distributions from during run, override this for Nexus or Artifactory | `https://www.python.org/ftp/python` |
| `python_pyenv_pythons` | Dict of pythons to install including checksum | See defaults |
| `python_pyenv_python_default_version` | Version of python to set as the default after install | `system` |
| `python_pyenv_tmpdir` | Temporary directory to use when building pythons | `/tmp` and see vars (distro specific) |
| `python_pyenv_plugins` | Dict of plugins to install (Git repos) | pyenv-virtualenv (see defaults) |

# Dependencies

None

# Example Playbook
```
    - hosts: all
      roles:
        - { role: bdellegrazie.python_pyenv }
```

# Use with Artifactory, Nexus or other Internal Mirror

Internal mirrors can be used to override the locations where data is retrieved

## Git repos
1. URL of pyenv: `python_pyenv_url`
2. URLs of pyenv plugins: `python_pyenv_plugins` - pyenv-virtualenv is installed by default and the Git repo URL is exposed as a separate variable for easy override (see defaults)
3. Pythons mirror URL: `python_pyenv_pythons_mirror_url` - Repo containing recipes to build various versions of Python, including upstream URLs as well as special dependencies locally mirrored for
convenience. This is essentially a static website constructed from a Git repo on Github.

The first two are easy and a straight copy of the repo will work, the third is not, the URLs inside the recipes need to be modified to point at internal mirrors for python downloads, readline etc.

Note that if system python versions are sufficient, use of Pyenv is an unnecessary complication - instead use virtualenv and Pipenv to manage dependencies within a virtual environment

# Testing

Testing is performed with [Molecule](https://github.com/ansible/molecule) using [Goss](https://github.com/aelsabbahy/goss) as a verifier

# License

GPLv3

Author Information
------------------

[Brett Delle Grazie](https://github.com/bdellegrazie/)
