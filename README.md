# SSHMonitorPy
> Monitors incoming ssh requests and will notify you on failed, successful or banned(IP via iptables/sshgaurd) attempts whether they're successful or not.
***

## Build program:

  **[anthony@ghost SSHMonitorPy]$** `sudo python setup.py install`

## Remove program:

  **[anthony@ghost SSHMonitorPy]$** `sudo python setup.py remove`

## Modify version in setup.py via vim/nano before building:
**`BEFORE(vim/nano setup.py):`**
```javascript
    setup(
        packages=[],
        name='sshmonitor',
        version='0.0.6', # increment version number
```
**`AFTER:`**
```javascript
    setup(
        packages=[],
        name='sshmonitor',
        version='0.0.7', # increment version number
```
## Build package for PyPi:

  **[anthony@ghost SSHMonitorPy]$** `sudo python setup.py sdist`
  
  **[anthony@ghost SSHMonitorPy]$** `twine upload dist/*`

**NOTE:** If twine does not work with the above command you can try,

   `twine upload --repository-url 'https://upload.pypi.org/legacy/' dist/sshmonitor-0.0.6.tar.gz`

## Contents of ~/.pypirc:
```javascript
[distutils]
index-servers =
  pypi
  pypitest

[pypi]
repository=https://pypi.python.org/pypi
username=username
password='password'

[pypitest]
repository=https://testpypi.python.org/pypi
username=username
password='password'
```
