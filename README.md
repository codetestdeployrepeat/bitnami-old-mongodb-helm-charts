# bitnami-old-mongodb-helm-charts
Index yaml for old mongodb helm charts from bitnami because the main index is too large

## Usage

We are using `jenkins-x` to manage our deployments. Here is an example of how we use this helm chart repo url.

Repo URL: https://raw.githubusercontent.com/lysender/bitnami-old-mongodb-helm-charts/master/mongodb

File: `jx-staging/helmfile.yaml`

```
filepath: ""
environments:
  default:
    values:
    - jx-values.yaml
repositories:
- name: lysender-mongodb
  url: https://raw.githubusercontent.com/lysender/bitnami-old-mongodb-helm-charts/master/mongodb
releases:
- chart: lysender-mongodb/mongodb
  version: 11.1.10
  name: user-service-mongodb
  namespace: jx-staging
  values:
  - user-service-mongodb-values.yaml
  - jx-values.yaml
templates: {}
renderedvalues: {}
```
