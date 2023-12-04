# Baseline-RE-for-BookInfo
Code for CS 395T's final project (CS 395T Advanced Topics in Computer Networks, Fall 2023). Some HTTP-based Redundancy Elimination algorithms tested on Istio's BookInfo.

With a properly set up BookInfo application (e.g., by following [this guide](https://istio.io/latest/docs/setup/getting-started/)), any of the filter configurations (specified by each `.yaml` file) can be applied via `kubectl apply`. For example:

```
kubectl apply -f lua_compression.yaml
```

To remove a specific filter:
```
kubectl delete -f [FILENAME]
```

To check applied filters:
```
kubectl get EnvoyFilter
```

To view logs (produced by `response_handle:logCritical()`):
```
kubectl logs -l app=[APP_NAME] -c istio-proxy
```
(`APP_NAME`: `reviews`, `productpage`, etc.)

Each filter configuration file includes comments on what is accomplished.

