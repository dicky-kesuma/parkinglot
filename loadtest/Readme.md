# Load Test Using vegeta

The installation can be found [here](https://github.com/tsenart/vegeta). 

## Writing test script
Create file *script.txt* and put the script load test on it.

```
POST http://localhsot:8080/parking/register
content-type: application/json
@registration.json
```

## Running the script


```
vegeta attack -rate=10 -duration=10m -timeout=2s -targets=script.txt | vegeta report
```

rate = Amount request persecond
duration = time request from the agent to the service
timeout = Deadline


