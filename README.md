# Simple OpenShift Build Pipeline Example

This simple Example shows how OpenShift Pipelines works

## Create Project

First you need to create a new OpenShift project

```
$ oc new-project sample-pipeline
```

## Create Pipeline

In this example we simple use the follwing yml to create the build. It's creates a Buildconfig with buildstratigy JenkinsPipeline, which references the `Jenkinsfile` located in this repository.

The pipeline itself just executes a few steps that write something into the log and wait for a few seconds. The only really interesting part is, that for the last three steps a dynamic `maven` build pod gets started and used as execution platform for those steps.

```
$ oc create -f buildconfig.yml
```

## Start the Pipeline


```
$ oc start-build appuio-sample-pipeline
```
