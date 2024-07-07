# TA_fiction docker tests

### Make sure:
- the docker and docker-compose are installed on system.

```commandline
pytest 
    <path to tests dir> 
    --tb=long
    --splunk-type=docker 
    --splunk-app=<addon name> 
    --splunk-password="Crest@12345"
    --splunk-data-generator=<path to pytest-splunk-addon-data.conf file from root> 
    --log-level=INFO 
    --junit-xml=test_dlp.xml
    -m splunk_searchtime_fields
    --search-interval=4
    --search-retry=4
    --search-index=*,_internal
    -v
```

```commandline
pytest tests --tb=long --splunk-type=docker --splunk-app=TA_fiction --splunk-password="Crest@12345" --splunk-data-generator="/workspaces/psa_examples/TA_fiction_docker/TA_fiction/default" --log-level=INFO --junit-xml=test_dlp.xml -m splunk_searchtime_fields --search-interval=4 --search-retry=4 --search-index=*,_internal -v
```

```commandline
docker ps -a --format '{{.ID}} -- {{.Names}} -- {{.Status}}'
```
