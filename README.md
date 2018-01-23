# zookeeper_recipe

## zookeeper watcher
```
/usr/bin/python child_watch.py
List of Children []
List of Children [u'child1']
List of Children [u'child1', u'child2']
List of Children [u'child1', u'child3', u'child2']
List of Children [u'child1', u'child2']
List of Children [u'child1']
List of Children []
```

On another terminal:
```
WatchedEvent state:SyncConnected type:None path:null

[zk: localhost:2181(CONNECTED) 0] create /MyPath/child1 ""
Created /MyPath/child1
[zk: localhost:2181(CONNECTED) 1] create /MyPath/child2 ""
Created /MyPath/child2
[zk: localhost:2181(CONNECTED) 2] create /MyPath/child3 ""
Created /MyPath/child3
[zk: localhost:2181(CONNECTED) 3] delete /MyPath/child3   
[zk: localhost:2181(CONNECTED) 4] delete /MyPath/child2
[zk: localhost:2181(CONNECTED) 5] delete /MyPath/child1
```

## zookeeper leader election
```
$ /usr/bin/python leader_election.py 
I am leader : 961165dc-c6f7-4858-a315-0be40fca1a47
961165dc-c6f7-4858-a315-0be40fca1a47 is still working
961165dc-c6f7-4858-a315-0be40fca1a47 is still working
961165dc-c6f7-4858-a315-0be40fca1a47 is still working
961165dc-c6f7-4858-a315-0be40fca1a47 is still working
961165dc-c6f7-4858-a315-0be40fca1a47 is still working
```
ctrl-C

Then another work will become leader

