# OpenSearch PoC

## Install the PoC

```shell
bash run
```

## Access OpenSearch Dashboard

```shell
kubectl -n opensearch port-forward svc/opensearch-dashboard-opensearch-dashboards 5601
```

## REST API

Check health:

```shell
kubectl proxy
curl https://127.0.0.1:8001/api/v1/namespaces/opensearch/services/https:opensearch-cluster-master:9200/proxy/_cluster/health
```
