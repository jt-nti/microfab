Experiment to get microfab running with the latest fabric binaries.

It would be nice to be able to run the `ibmcom/ibp-microfab` image unchanged with a volumn mount, something like this:

```
docker run --name microfab --rm -v ${PWD}/fabric-unstable:/opt/fabric -p 8080:8080 -e MICROFAB_CONFIG ibmcom/ibp-microfab
```

That currently doesn't work because the `/var/hyperledger` cannot be created at startup due to permission problems.
Maybe that directory is configurable instead?
Building an `unstable-mircofab` image works for now instead but seems a bit overkill.
