mkdir mongoexam

cd mongoexam

pwd

mkdir data

파일전송 프로그램 Fz



mongoDB client program 명 : mongo

> mongo

> show dbs
> 





```

> mongo

> show dbs
> use testdb_lab05(db있으면 그거 이용상태로 바뀜 ,없으면 새로 만듬)
> db
> show dbs(아직 도큐먼트가 없어서 리스트에 안나옴)
> db.book.insert({"name": "python", "price": 10000})
> show collections (최초 insert시 안만들어진거 자동으로 생김)




>quit()

```

``` 
login as: lab05
Authenticating with public key "imported-openssh-key"
Last login: Tue Nov 10 16:03:53 2020 from 125.143.140.216
[lab05@ip-172-31-42-102 ~]$ conda activate awsvenv
(awsvenv) [lab05@ip-172-31-42-102 ~]$ conda install pymongo
```




``` 
login as: lab05
Authenticating with public key "imported-openssh-key"
Last login: Tue Nov 10 10:22:17 2020 from 125.132.118.94
[lab05@ip-172-31-42-102 ~]$ pwd
/home/lab05
[lab05@ip-172-31-42-102 ~]$ db
-bash: db: command not found
[lab05@ip-172-31-42-102 ~]$ mkdir mongoexam
[lab05@ip-172-31-42-102 ~]$ ls
data  mongoexam  mydir  PyStexam  test.txt
[lab05@ip-172-31-42-102 ~]$ cd mongoexam
[lab05@ip-172-31-42-102 mongoexam]$ pwd
/home/lab05/mongoexam
[lab05@ip-172-31-42-102 mongoexam]$ mkdir data
[lab05@ip-172-31-42-102 mongoexam]$ ls data
emp.csv  iris.csv
[lab05@ip-172-31-42-102 mongoexam]$ cd data
[lab05@ip-172-31-42-102 data]$ mongo
MongoDB shell version v4.0.21
connecting to: mongodb://127.0.0.1:27017/?gssapiServiceName=
Implicit session: session { "id" : UUID("f1e98724-e00b-4e88-}
MongoDB server version: 4.0.21
Welcome to the MongoDB shell.
For interactive help, type "help".
For more comprehensive documentation, see
        http://docs.mongodb.org/
Questions? Try the support group
        http://groups.google.com/group/mongodb-user
Server has startup warnings:
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] ** Wis bound to localhost.
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **  ms will be unable to connect to this server.
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **  rver with --bind_ip <address> to specify which IP
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **   should serve responses from, or with --bind_ip_all to
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **  interfaces. If this behavior is desired, start the
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **  --bind_ip 127.0.0.1 to disable this warning.
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] ** Wmm/transparent_hugepage/enabled is 'always'.
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] **  ting it to 'never'
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] ** Wmm/transparent_hugepage/defrag is 'always'.
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] **  ting it to 'never'
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] ** W too low. rlimits set to 4096 processes, 64000 files. Number be at least 32000 : 0.5 times number of files.
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
---
Enable MongoDB's free cloud-based monitoring service, which d display
metrics about your deployment (disk utilization, CPU, operat.

The monitoring data will be available on a MongoDB website wessible to you
and anyone you share the URL with. MongoDB may use this infouct
improvements and to suggest MongoDB products and deployment

To enable free monitoring, run the following command: db.ena
To permanently disable this reminder, run the following commonitoring()
---

> show dbs
admin   0.000GB
config  0.000GB
local   0.000GB
> use testdb_lab05
switched to db testdb_lab05
> db
testdb_lab05
> show dbs
admin   0.000GB
config  0.000GB
local   0.000GB
> db.book.insert({"name": "python", "price": 10000})
WriteResult({ "nInserted" : 1 })
> show dbs
admin         0.000GB
config        0.000GB
local         0.000GB
testdb_lab04  0.000GB
testdb_lab05  0.000GB
testdb_lab06  0.000GB
> show collections
book
> db.book.insert({"name": "java", "price": 12000})
WriteResult({ "nInserted" : 1 })
> ": "javascript", "price": 8000})db.book.insert({"name": "j 8000})
2020-11-10T16:35:41.037+0900 E QUERY    [js] SyntaxError: miment @(shell):1:4
> db.book.insert({"name": "javascript", "price": 8000})
WriteResult({ "nInserted" : 1 })
> db.book.insert({"name": "html5", "price": 8000})
WriteResult({ "nInserted" : 1 })
> db.book.insert({"name": "django", "price": 20000})
WriteResult({ "nInserted" : 1 })
> db.book.insert({"name": "spark", "price": 25000})
WriteResult({ "nInserted" : 1 })
> db.book.find()
{ "_id" : ObjectId("5faa41fbe0f10333b7c5a58d"), "name" : "py00 }
{ "_id" : ObjectId("5faa42b9e0f10333b7c5a58e"), "name" : "ja }
{ "_id" : ObjectId("5faa42dee0f10333b7c5a58f"), "name" : "ja 8000 }
{ "_id" : ObjectId("5faa42e7e0f10333b7c5a590"), "name" : "ht }
{ "_id" : ObjectId("5faa42f1e0f10333b7c5a591"), "name" : "dj00 }
{ "_id" : ObjectId("5faa42fae0f10333b7c5a592"), "name" : "sp0 }
> db.book.find().pretty()
{
        "_id" : ObjectId("5faa41fbe0f10333b7c5a58d"),
        "name" : "python",
        "price" : 10000
}
{
        "_id" : ObjectId("5faa42b9e0f10333b7c5a58e"),
        "name" : "java",
        "price" : 12000
}
{
        "_id" : ObjectId("5faa42dee0f10333b7c5a58f"),
        "name" : "javascript",
        "price" : 8000
}
{
        "_id" : ObjectId("5faa42e7e0f10333b7c5a590"),
        "name" : "html5",
        "price" : 8000
}
{
        "_id" : ObjectId("5faa42f1e0f10333b7c5a591"),
        "name" : "django",
        "price" : 20000
}
{
        "_id" : ObjectId("5faa42fae0f10333b7c5a592"),
        "name" : "spark",
        "price" : 25000
}
> db.book.find().sort({"price": 1})
{ "_id" : ObjectId("5faa42dee0f10333b7c5a58f"), "name" : "ja 8000 }
{ "_id" : ObjectId("5faa42e7e0f10333b7c5a590"), "name" : "ht }
{ "_id" : ObjectId("5faa41fbe0f10333b7c5a58d"), "name" : "py00 }
{ "_id" : ObjectId("5faa42b9e0f10333b7c5a58e"), "name" : "ja }
{ "_id" : ObjectId("5faa42f1e0f10333b7c5a591"), "name" : "dj00 }
{ "_id" : ObjectId("5faa42fae0f10333b7c5a592"), "name" : "sp0 }
> db.book.find().sort({"price": -1, "name": 1})
{ "_id" : ObjectId("5faa42fae0f10333b7c5a592"), "name" : "sp0 }
{ "_id" : ObjectId("5faa42f1e0f10333b7c5a591"), "name" : "dj00 }
{ "_id" : ObjectId("5faa42b9e0f10333b7c5a58e"), "name" : "ja }
{ "_id" : ObjectId("5faa41fbe0f10333b7c5a58d"), "name" : "py00 }
{ "_id" : ObjectId("5faa42e7e0f10333b7c5a590"), "name" : "ht }
{ "_id" : ObjectId("5faa42dee0f10333b7c5a58f"), "name" : "ja 8000 }
> db.book.insert({"name": "CSS3", "price": 17000})
WriteResult({ "nInserted" : 1 })
> db.book.insert([
...  {"name": "pandas", "price": 21000},
...  {"name": "R", "price": 23000}
...  ])
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 2,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
> db.books.find()
> db.book.find()
{ "_id" : ObjectId("5faa41fbe0f10333b7c5a58d"), "name" : "py00 }
{ "_id" : ObjectId("5faa42b9e0f10333b7c5a58e"), "name" : "ja }
{ "_id" : ObjectId("5faa42dee0f10333b7c5a58f"), "name" : "ja 8000 }
{ "_id" : ObjectId("5faa42e7e0f10333b7c5a590"), "name" : "ht }
{ "_id" : ObjectId("5faa42f1e0f10333b7c5a591"), "name" : "dj00 }
{ "_id" : ObjectId("5faa42fae0f10333b7c5a592"), "name" : "sp0 }
{ "_id" : ObjectId("5faa454de0f10333b7c5a593"), "name" : "CS }
{ "_id" : ObjectId("5faa458ae0f10333b7c5a594"), "name" : "pa00 }
{ "_id" : ObjectId("5faa458ae0f10333b7c5a595"), "name" : "R"
> quit()
[lab05@ip-172-31-42-102 data]$ pwd
/home/lab05/mongoexam/data
[lab05@ip-172-31-42-102 data]$ mongoimport -d testdb_lab05 -ile emp.csv –headerline
2020-11-10T17:07:29.718+0900    error validating settings: m, --fieldFile or --headerline to import this file type
2020-11-10T17:07:29.718+0900    try 'mongoimport --help' for
[lab05@ip-172-31-42-102 data]$ ^C
[lab05@ip-172-31-42-102 data]$ mongoimport -d testdb_lab05 -ile emp.csv –headerline
2020-11-10T17:08:51.680+0900    error validating settings: m, --fieldFile or --headerline to import this file type
2020-11-10T17:08:51.680+0900    try 'mongoimport --help' for
[lab05@ip-172-31-42-102 data]$ mongoimport -d testdb_lab05 -file iris.csv –headerlinemongoimport -d testdb_lab05 -c irisris.csv –headerline
2020-11-10T17:09:06.279+0900    error validating settings: m, --fieldFile or --headerline to import this file type
2020-11-10T17:09:06.279+0900    try 'mongoimport --help' for
[lab05@ip-172-31-42-102 data]$ pwd
/home/lab05/mongoexam/data
[lab05@ip-172-31-42-102 data]$ mongoimport -d testdb_lab05 -ile emp.csv --headerline
2020-11-10T17:11:59.697+0900    connected to: localhost
2020-11-10T17:11:59.705+0900    imported 14 documents
[lab05@ip-172-31-42-102 data]$ mongoimport -d testdb_lab05 -file iris.csv --headerline
2020-11-10T17:12:11.977+0900    connected to: localhost
2020-11-10T17:12:11.987+0900    imported 150 documents
[lab05@ip-172-31-42-102 data]$ show dbs
-bash: show: command not found
[lab05@ip-172-31-42-102 data]$ db
-bash: db: command not found
[lab05@ip-172-31-42-102 data]$ show collections
-bash: show: command not found
[lab05@ip-172-31-42-102 data]$ use testdb_lab05
-bash: use: command not found
[lab05@ip-172-31-42-102 data]$ quit()
> pwd
-bash: syntax error near unexpected token `pwd'
[lab05@ip-172-31-42-102 data]$ pwd
/home/lab05/mongoexam/data
[lab05@ip-172-31-42-102 data]$ mongo
MongoDB shell version v4.0.21
connecting to: mongodb://127.0.0.1:27017/?gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("821fb0a9-7d61-4359-9f01-47c0d4031251") }
MongoDB server version: 4.0.21
Server has startup warnings:
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] ** WARNING: This server is bound to localhost.
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **          Remote systems will be unable to connect to this server.
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **          Start the server with --bind_ip <address> to specify which IP
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **          addresses it should serve responses from, or with --bind_ip_all to
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **          bind to all interfaces. If this behavior is desired, start the
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten] **          server with --bind_ip 127.0.0.1 to disable this warning.
2020-11-10T08:52:10.792+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] ** WARNING: /sys/kernel/mm/transparent_hugepage/enabled is 'always'.
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] **        We suggest setting it to 'never'
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] ** WARNING: /sys/kernel/mm/transparent_hugepage/defrag is 'always'.
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] **        We suggest setting it to 'never'
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten] ** WARNING: soft rlimits too low. rlimits set to 4096 processes, 64000 files. Number of processes should be at least 32000 : 0.5 times number of files.
2020-11-10T08:52:10.793+0900 I CONTROL  [initandlisten]
---
Enable MongoDB's free cloud-based monitoring service, which will then receive and display
metrics about your deployment (disk utilization, CPU, operation statistics, etc).

The monitoring data will be available on a MongoDB website with a unique URL accessible to you
and anyone you share the URL with. MongoDB may use this information to make product
improvements and to suggest MongoDB products and deployment options to you.

To enable free monitoring, run the following command: db.enableFreeMonitoring()
To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---

> cd
[native code]
> quit()
[lab05@ip-172-31-42-102 data]$ cd
[lab05@ip-172-31-42-102 ~]$ pwd
/home/lab05
[lab05@ip-172-31-42-102 ~]$ ls
data  mongoexam  mydir  PyStexam  test.txt
[lab05@ip-172-31-42-102 ~]$ conda activate
(base) [lab05@ip-172-31-42-102 ~]$  jupyter lab --ip=0.0.0.0 --no-browser --port=8894
[I 17:33:47.962 LabApp] Writing notebook server cookie secret to /run/user/1011/jupyter/notebook_cookie_secret
[I 17:33:48.916 LabApp] JupyterLab extension loaded from /home/centos/anaconda3/lib/python3.7/site-packages/jupyterlab
[I 17:33:48.916 LabApp] JupyterLab application directory is /home/centos/anaconda3/share/jupyter/lab
[W 17:33:48.917 LabApp] JupyterLab server extension not enabled, manually loading...
[I 17:33:48.920 LabApp] JupyterLab extension loaded from /home/centos/anaconda3/lib/python3.7/site-packages/jupyterlab
[I 17:33:48.920 LabApp] JupyterLab application directory is /home/centos/anaconda3/share/jupyter/lab
[I 17:33:48.920 LabApp] Serving notebooks from local directory: /home/lab05
[I 17:33:48.920 LabApp] The Jupyter Notebook is running at:
[I 17:33:48.920 LabApp] http://(ip-172-31-42-102.ap-northeast-2.compute.internal or 127.0.0.1):8894/?token=cc665e06cbee9e615edac606b7c9f6c3cd801c6954caaed5
[I 17:33:48.920 LabApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 17:33:48.924 LabApp]

    To access the notebook, open this file in a browser:
        file:///run/user/1011/jupyter/nbserver-4788-open.html
    Or copy and paste one of these URLs:
        http://(ip-172-31-42-102.ap-northeast-2.compute.internal or 127.0.0.1):8894/?token=cc665e06cbee9e615edac606b7c9f6c3cd801c6954caaed5
 http://(ip-172-31-42-102.ap-northeast-2.compute.internal or 127.0.0.1):8894/?token=cc665e06cbee9e615edac606b7c9f6c3cd801c6954caaed5[I 17:35:15.411 LabApp] 302 GET /?token=cc665e06cbee9e615edac606b7c9f6c3cd801c6954caaed5 (125.143.140.216) 0.62ms
[W 17:35:20.093 LabApp] Could not determine jupyterlab build status without nodejs
[I 17:35:27.092 LabApp] Creating new notebook in /
[I 17:35:28.577 LabApp] Kernel started: 82106d48-aa83-4e2f-8b7d-bad42ed84411
[I 17:35:43.504 LabApp] Uploading file to /mongo_aws.ipynb
[I 17:37:28.876 LabApp] Saving file at /Untitled.ipynb
[W 17:38:39.321 LabApp] Notebook mongo_aws.ipynb is not trusted
[I 17:38:56.780 LabApp] Kernel started: b0d7a3bb-4a12-4015-a7dd-dacab13c8201
[I 17:40:47.850 LabApp] Saving file at /mongo_aws.ipynb
[I 17:41:04.634 LabApp] Uploading file to /data/hankuk1_geo.json
[I 17:42:48.018 LabApp] Saving file at /mongo_aws.ipynb
[I 17:44:48.220 LabApp] Saving file at /mongo_aws.ipynb
[I 17:46:48.415 LabApp] Saving file at /mongo_aws.ipynb
[I 17:48:48.625 LabApp] Saving file at /mongo_aws.ipynb
[I 17:50:48.790 LabApp] Saving file at /mongo_aws.ipynb
[I 17:52:49.625 LabApp] Saving file at /mongo_aws.ipynb
[I 17:54:49.780 LabApp] Saving file at /mongo_aws.ipynb


```

