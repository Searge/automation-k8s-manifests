# Automation k8s manifests

## Prompts portfolio

| NAME                    | PROMPT                                                                                                                | DESCRIPTION                             | EXAMPLE                                                 |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------- | ------------------------------------------------------- |
| app.yaml                | create deploy with 2 replicas of demo app which expose 80 port from 8080; registry: gcr.io/venture-clouds/demo:v2.0.0 | Create simple app                       | [app.yaml](yaml/app.yaml)                               |
| app-livenessProbe.yaml  | create liveness probe for the demo app pod                                                                            | Creates liveness probe                  | [app-livenessProbe.yaml](yaml/app-livenessProbe.yaml)   |
| app-readinessProbe.yaml | create readiness probe for the demo-app pods                                                                          | Configures a readines probe             | [app-readinessProbe.yaml](yaml/app-readinessProbe.yaml) |
| app-volumeMounts.yaml   | create volume mounts for master pod of the demo-app                                                                   | Defines volumes mounts                  | [app-volumeMounts.yaml](yaml/app-volumeMounts.yaml)     |
| app-cronjob.yaml        | create resource for schedulling liveness probe and readlines probes                                                   | Scheduling jobs                         | [app-cronjob.yaml](yaml/app-cronjob.yaml)               |
| app-job.yaml            | create rsync job for demo-app form google cloud folder                                                                | Simple job                              | [app-job.yaml](yaml/app-job.yaml)                       |
| app-multicontainer.yaml | create multicontainer with django app named django-front which are runing on 2 repliacas with shared aws efs volume,  | Create some overengineer multicontainer | [app-multicontainer.yaml](yaml/app-multicontainer.yaml) |
|                         | one solr replica, mongodb with master pod and slave pod replicas, envoy as webserver for two fronts and loadbalancer. |                                         |                                                         |
|                         | Implement all needed ports and volumes.                                                                               |                                         |                                                         |
| app-resources.yaml      | create resource limits for django-front                                                                               | Defines resource limits                 | [app-resources.yaml](yaml/app-resources.yaml)           |
| app-secret-env.yaml     | use secrets to set environment variables. Do not use base64 data, just uppercase variables                            | Defines secrets                         | [app-secret-env.yaml](yaml/app-secret-env.yaml)         |
| app-mongodb.yml         | create deploy MongoDB with pvc, replica set, etc                                                                      | Define mongodb instances                | [app-mongodb.yml](yaml/app-mongodb.yml)                 |
