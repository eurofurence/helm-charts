# Eurofurence Mobile App Backend Helm Charts

Simplify deployment of the backend for the [Eurofurence mobile app](https://app.eurofurence.org) on Kubernetes by using this Helm chart, which allows multiple parallel deployments under the same domain and integration with Infisical for secrets and config maps.

## Pre-requisites and External Dependencies

The chart currently expects dependencies like the database server and S3/MinIO to be deployed externally and configured via the secrets.
Some of these dependencies may also be installed as optional part of this chart in the future, but for mostly for development purposes.

## Configuration via `values.yaml`

See comments in [`values.yaml`](./charts/mobile-app/values.yaml) file.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  `helm repo add eurofurence https://eurofurence.github.io/helm-charts`

If you had already added this repo earlier, run `helm repo update` to retrieve the latest versions of the packages.
You can then run `helm search repo eurofurence` to see the charts.

To install the `mobile-app` chart:

  `helm install my-mobile-app eurofurence/mobile-app`

To uninstall the chart:

  `helm uninstall my-mobile-app`
