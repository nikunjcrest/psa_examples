# PSA Examples
## External (external)
Create saprate virtual environment for external tests
```commandline
python3 -m venv venv_psa_external
```
install PSA SDK and other pkgs
```commandline
pip install pytest-splunk-addon pytest-xdist pytest-expect
```

## Docker (docker)
Create saprate virtual environment for docker tests
```commandline
python3 -m venv venv_psa_docker
```
install PSA SDK and other pkgs
```commandline
pip install "pytest-splunk-addon[docker]" pytest-xdist pytest-expect
```



<br>
<br>
<br>

---

```commandline
rm -fr ./.pytest_cache ./.tokenized_events ./uf_files ./events.pickle ./generator.lock ./pytest_splunk_addon.log ./splunksplwrapper.log ./tests/__pycache__ ./test_dlp.xml ./*ac_*
```
---