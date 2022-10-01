# Build instructions - DRAFT

```bash
python3 -m venv .venv
. .venv/bin/activate
pip3 install --upgrade setuptools wheel pip jupyter_packaging~=0.7.9 jupyterlab 
npm clean-install
python3 setup.py sdist bdist_wheel
pip3 install dist/*.whl
```

[On Linux, you need to edit your /etc/ssl/openssl.cnf to un-comment a few lines that will enable legacy provider support.](https://stackoverflow.com/questions/72866798/node-openssl-legacy-provider-is-not-allowed-in-node-options#answer-73064710)

```properties
##[provider_sect]
##default = default_sect
##legacy = legacy_sect
##
##[default_sect]
##activate = 1
##
##[legacy_sect]
##activate = 1
```
