# OpenShiftProxy
This repo realize the app necessary to NoMishap project for OpenShift PaaS

Due to absence of an conversion app from pdf to text only in the case of Openshift we take care of realize it.
To deploy the app:
- go to openshift online
- create new project
- fill the name field=>create
- choose js project 
- fill name project and cut and paste git url in the git field(the git must be public or you must authoraize it)
- click create and wait until openshift deploy all nec pods
- go to application=>routes
- and create 2 routes
  - /ping
  - /pdftotext

- the name is arbitrary 

- hostname is automatic 

- fill Path with /ping or /pdftotext

- and then click Create

  ENV variables:

process.env.SERVICE = url of the pdf service

process.env.NODE_ENV=== 'production'=> boolean production or not
process.env.PORT= port where the service should listen if not setted try to request to paas provider otherwise use 3000 as def
process.env.NAME= name of the service used by elk in apm module
