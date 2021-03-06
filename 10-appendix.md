#Appendix: OpenShift Client Commands Used

Take it as a small reference: Here you find all commands used, in a chronological and in an alphabetical order:

## Commands in Chronological Order
Here are all commands we used in the workshop in the order of their first appearance. 

NB - recurring commands are **not** listed except of commands used with new/different parameters.


### Lab 1
```
$ oc version
```
### Lab 2

```
$ oc login https://openshift-master.demo.openshift.me
```
```
$ oc login https://openshift-master.demo.openshift.me --insecure-skip-tls-verify=true
```
```
$ oc project userXX-smoke
```
```
$ oc get routes
```

### Lab 3
```
$ oc get pods
```
```
$ oc get pod smoke-1-XYZXY -o json
```
```
$ oc new-project userXX-guestbook
```
```
$ oc get projects
```
```
$ oc new-app kubernetes/guestbook
```
```
$ oc get services
```
```
$ oc get service guestbook -o json
```
```
$ oc describe service guestbook
```
### Lab 4
```
$ oc expose service guestbook
```
### Lab 5
```
$ oc get rc
```
```
$ oc get rc guestbook-1 -o json
```
```
$ oc get rc guestbook-1 -o json | grep -B1 -E "replicas" | grep -v Docker
```
```
$ oc scale --replicas=3 rc guestbook-1
```
```
$ oc delete pod guestbook-1-a163w
```
### Lab 6
```
$ oc new-app jboss-eap64-openshift~https://github.com/YOURUSER/openshift3mlbparks.git
```
```
$ oc get builds
```
```
$ oc build-logs openshift3mlbparks-1
```
### Lab 7
```
$ oc new-app mongodb -e MONGODB_USER=mlbparks -e MONGODB_PASSWORD=mlbparks -e MONGODB_DATABASE=mlbparks -e MONGODB_ADMIN_PASSWORD=mlbparks
```
```
$ oc get pods --watch
```
```
$ oc get dc
```
```
$ oc env dc openshift3mlbparks -e MONGODB_USER=mlbparks -e MONGODB_PASSWORD=mlbparks -e MONGODB_DATABASE=mlbparks
```
```
$ oc get dc openshift3mlbparks -o json
```

Unix:

```
$ oc exec -tip mongodb-24-rhel7-1-73af9  -- bash -c 'mongo -u mlbparks -p mlbparks mlbparks'
```

Windows:

```
$ oc exec -tip mongodb-24-rhel7-1-73af9  -- bash -c "mongo -u mlbparks -p mlbparks mlbparks"
```
### Lab 9
```
$ oc create -f https://raw.githubusercontent.com/gshipley/openshift3mlbparks/master/mlbparks-template.json
```


## Commands in Alphabetical Order
All commands used in the workshop - please use ```oc help <command>``` to get some basic information or check the [documentation](https://docs.openshift.com/enterprise/3.1/cli_reference/index.html).


```
$ oc build-logs openshift3mlbparks-1
```

```
$ oc create -f https://raw.githubusercontent.com/gshipley/openshift3mlbparks/master/mlbparks-template.json
```
```
$ oc delete pod guestbook-1-a163w
```
```
$ oc describe service guestbook
```
```
$ oc env dc openshift3mlbparks -e MONGODB_USER=mlbparks -e MONGODB_PASSWORD=mlbparks -e MONGODB_DATABASE=mlbparks
```
---
Unix:

```
$ oc exec -tip mongodb-24-rhel7-1-73af9  -- bash -c 'mongo -u mlbparks -p mlbparks mlbparks'
```

Windows:

```
$ oc exec -tip mongodb-24-rhel7-1-73af9  -- bash -c "mongo -u mlbparks -p mlbparks mlbparks"
```
---

```
$ oc expose service guestbook
```

---

```
$ oc get builds
```
```
$ oc get dc
```
```
$ oc get dc openshift3mlbparks -o json
```
```
$ oc get pod smoke-1-XYZXY -o json
```
```
$ oc get pods
```
```
$ oc get pods --watch
```
```
$ oc get projects
```
```
$ oc get rc
```
```
$ oc get rc guestbook-1 -o json
```
```
$ oc get rc guestbook-1 -o json | grep -B1 -E "replicas" | grep -v Docker
```
```
$ oc get routes
```
```
$ oc get services
```
```
$ oc get service guestbook -o json
```
---
```
$ oc login https://openshift-master.demo.openshift.me
```
```
$ oc login https://openshift-master.demo.openshift.me --insecure-skip-tls-verify=true
```
---
```
$ oc new-app kubernetes/guestbook
```
```
$ oc new-app jboss-eap64-openshift~https://github.com/YOURUSER/openshift3mlbparks.git
```
```
$ oc new-app mongodb -e MONGODB_USER=mlbparks -e MONGODB_PASSWORD=mlbparks -e MONGODB_DATABASE=mlbparks -e MONGODB_ADMIN_PASSWORD=mlbparks
```
---
```
$ oc new-project userXX-guestbook
```
```
$ oc project userXX-smoke
```
```
$ oc scale --replicas=3 rc guestbook-1
```
```
$ oc version
```




