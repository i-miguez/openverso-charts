# open5gs and srsLTE 

5G end to end communication demo with open5gs and srsLTE.

# Deployment EPC and register subscribers

deploy the EPC core (open5gs) with:

```
helm3 install --name epc --namespace test --values epc_values.yaml ../charts/open5gs/
```

Register subscriber in epc with `/register_subscriber.sh`.


# Deployment RAN

Deploy with

```
helm3 install --name lte --namespace test ../charts/srs-lte/ --values lte_values.yaml
```

Undeploy with:

```
helm3 delete --purge lte 
```