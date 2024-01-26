explaination about helm

Helm is a package manager in kubernetes
adavanatages of helm are
* Manage complexity
* Easy updates
* simple sharing
* Rollbacks

Three Big concepts in helm are

* helm Charts
* Helm Repositories
* Helm Release

  Helm chart : A chart is helm package it conatins all of the resource definitations neccessary to run the application
  Helm Repository: It is the place where charts can be collected and shared
  Helm Release : A release is an instance of chart runnng in a kubernetes cluster

In general helm install charts into kubernetes and create a new release for each installation

Helm documentation
https://helm.sh/

Uses of yaml


# Helm chart
   Bundle of Yaml files
   Create your own helm charts with helm
   Push them to helm repositories

# Template engine

   if the application has many microservices and the deployment.yaml and service.yaml is same for all the services and there is only change in the name of the application then values.yaml file can be used and can be replaced with the dynamic values when need

# It can be used when same application has to be  deployed in different environment(dev,stage, prod)

# Helm Chart Structure

mychart/          -   (Top level mychart folder -name of the chart)
  chart.yaml      -    meta info about chart such as name ,version and dependenices
  values.yaml     -    values for the template files they can be overwritten
  charts /        -    it contains chart dependencies
  templates /     -    it contains actual template files

  # helm install <chartname> command can be used to deploy the applications to kubernets

  # Helm has even release management feature

  # Helm version 3 is the latest version, Tiller has been removed, making Helm easier to install and use.

  Install the helm on windows using binary and then set it as system environment variables

  Then enter "helm create helm-guestbook" command it creates the folder with directory structure
  