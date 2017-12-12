= Workshop app
Microservice application consisting of 3 componentes (microservices):

- parksmap: web frontend with embedded Java API Gateway. One single deployment. Running on Wildfly application server.
- nationalparks: backend with REST gateway and mongodb. The REST gateway is built from source in Python. Uses a Secret and a PVC.
- mlbparks: backend with REST gateway and mongodb. The REST gateway is built from source in Python. Uses a ConfigMap.

![architecture](workshop-app-architecture.png)

== Deploy
To deploy the 3 components do:

```
oc apply -f workshop-parksmap.yaml
oc apply -f workshop-nationalparks.yaml
oc apply -f workshop-mlbparks.yaml
```

You can install any of the 3 components (microservices) independently or all together.

In case you just want copy and paste a link from GitHub, use:

```
oc apply -f https://raw.githubusercontent.com/jorgemoralespou/ose-sample-apps-layouts/master/workshop-app/workshop-parksmap.yaml
oc apply -f https://raw.githubusercontent.com/jorgemoralespou/ose-sample-apps-layouts/master/workshop-app/workshop-nationalparks.yaml
oc apply -f https://raw.githubusercontent.com/jorgemoralespou/ose-sample-apps-layouts/master/workshop-app/workshop-mlbparks.yaml
```


