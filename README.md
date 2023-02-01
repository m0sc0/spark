# SPARK CHEATPAGE
## HDFS (Hadoop Distributed File System)
It replicate the data on 3 DataNodes  
DataNode directories  

Commands:
```
hdfs dfs -du -h <path>
hdfs dfs -rm -skipTrash <path>
```

## YARN (Yet Another Resource Negotiator)
YARN enables multiple data access applications to process it.  
Resource Manager keeps the meta info about which jobs are running on which Node Manage and how much memory and CPU is consumed and hence has a holistic view of total CPU and RAM consumption of the whole cluster.  
UI: Here we see the running jobs  

### YARN UI
![YARN UI](https://github.com/m0sc0/spark/blob/main/yarn%20ui.jpg)
## AMBARI
To manage all the modules  

```
hdfs dfsadmin -report
systemctl status ambari-agent
If is all down on ambari:  
1) Start HDF
2) If there is not active NameNode, run the following command from NameNode1 server ONLY IT IS REQUIRED (run it on sparkmaster): sudo -u hdfs hdfs haadmin  -ns nameservice1 -transitionToActive --forceactive nn1 --forcemanual  
```
