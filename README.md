stepic-pytest
=============

Test scenario runner for Stepic Linux challenge.

## Install
```bash
mkvirtualenv --python=/usr/bin/python2.7 stepic-linux
pip install https://github.com/StepicOrg/stepic-pytest/archive/master.zip
```

## Usage
Run a test scenario that checks `localhost`, the test scenario is located in the file `test_scenario.py`:
```bash
py.test -s -z --assert plain --server localhost --ssh-key local test_scenario.py
```
Or run a test scenario that checks a remote server `HOSTNAME` using SSH key `~/.ssh/id_rsa`:
```bash
py.test -s -z --assert plain --server HOSTNAME --ssh-key ~/.ssh/id_rsa test_scenario.py
```
There is an extra option `--zoe-report` for the pytest command that prints a special structure used by Stepic to retrieve a check result and feedback message.
