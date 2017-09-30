# Simple OpenShift Build Pipeline Example

This simple Example shows how OpenShift Pipelines works

## Create Project

First you need to create a new OpenShift project

```
$ oc new-project sample-pipeline
```

## Create Pipeline

In this example we simple use the follwing yml to create the build. It's creates a Buildconfig with buildstratigy JenkinsPipeline, which references the Jenkinsfile located in this repository.

```
$ oc create -f buildconfig.yml
```

## Start the Pipeline


```
$ oc start-build appuio-sample-pipeline
```
