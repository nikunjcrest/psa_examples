# TA_fiction external tests

### Make sure:
- the splunk instance is up and running properly.
- the TA_fiction app/addon is installed in splunk instance.

```
pytest 
    <path to tests dir> 
    --splunk-type=external 
    --splunk-app=<addon name> 
    --splunk-data-generator=<path to pytest-splunk-addon-data.conf file from root> 
    --splunk-host=<VM ip of localhost ip> 
    --splunk-port=<splunk manajment port ex 8089> 
    --splunk-user=admin 
    --splunk-password="Crest@12345" 
    --splunk-hec-token=<hec token from splunk [data inputs > http-eventcollector]> 
    --log-level=INFO 
    --junit-xml=test_dlp.xml
    -m splunk_searchtime_fields
    --search-interval=4
    --search-retry=4
    --search-index=*,_internal
    -v
    -n 2
```

```
pytest tests --splunk-type=external --splunk-app=TA_fiction --splunk-data-generator="/opt/Projects/nikunj_psa_examples/TA_fiction_external/TA_fiction/default" --splunk-host=10.50.9.187 --splunk-port=8089 --splunk-user=admin --splunk-password="Crest@12345" --splunk-hec-token=1c91316e-73f5-4576-9fea-a4da88a5a133 --log-level=INFO --junit-xml=test_dlp.xml -m splunk_searchtime_fields --search-interval=4 --search-retry=4 --search-index=*,_internal -v -n 2
```