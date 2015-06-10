# gapcio

`gapcio` is a simple shell script that helps manage SSH keys using Github as
a central point. It is meant as an alternative to manualy copying keys with
`scp` or `ssh-copy-id`.

## Install

Copy `gapcio` script to a directory under your `PATH`.

## Usage

* `get <username>` Fetch and display public keys for given user
* `add <username> [authorized_keys_path]` Add public keys of given user to `authorized_keys_path` (by default `~/.ssh/authorized_keys)
* `delete <username> [authorized_keys_path]` Delete all public keys of given user from `authorized_keys_path` (by default `~/.ssh/authorized_keys)

## Example

Add all public keys from `zaiste` user on Github to `~/.ssh/authorized_keys` on
the current machine.

    gapcio add zaiste

## ToDo

- [ ] GitHub Enterprise support
- [ ] Verify if keys already exist
- [ ] Ability to manage single keys
- [ ] Custom comments SSH support
