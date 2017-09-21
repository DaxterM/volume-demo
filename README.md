=============
Persistent Volume Demo
=============

A sample application demonstrating persistent volumes. 
```
$ git clone https://github.com/DaxterM/volume-demo/
$ cd volume-demo
$ mvn install

$ cf push --no-start
$ cf create-service nfs Existing volume-service -c '{"share":"10.193.53.248/export/vol1"}'
$ cf bind-service volume-demo volume-service -c '{"uid":"1000","gid":"1000"}'
$ cf start volume-demo
```
