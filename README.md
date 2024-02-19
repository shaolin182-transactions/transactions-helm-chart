## Useful commands

```shell
# Generate files
helm template -f values.yaml -f values-secrets.yaml .

# Package chart, use Chart.yaml file for getting some information
helm package .

# Install app through local chart
helm install -f values.yaml -f values-secrets.yaml -n transactions transactions-test transactions-helm-chart-0.1.0.tgz --create-namespace

# List installed app
helm list

# Uninstall app
helm uninstall -n transactions transactions-test

# Upgrade app
# From transactions-helm-chart directory
helm upgrade -n transactions transactions-test transactions-helm-chart-0.1.0.tgz -f values.yaml -f values-secrets.yaml
```