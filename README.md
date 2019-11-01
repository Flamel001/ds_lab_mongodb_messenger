# ds_lab_mongodb_messenger

rs.status() before shutting machines:
```
{
        "set" : "rs0",
        "date" : ISODate("2019-11-01T07:14:40.368Z"),
        "myState" : 1,
        "term" : NumberLong(1),
        "syncingTo" : "",
        "syncSourceHost" : "",
        "syncSourceId" : -1,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572592475, 1),
                        "t" : NumberLong(1)
                },
                "lastCommittedWallTime" : ISODate("2019-11-01T07:14:35.324Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572592475, 1),
                        "t" : NumberLong(1)
                },
                "readConcernMajorityWallTime" : ISODate("2019-11-01T07:14:35.324Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572592475, 1),
                        "t" : NumberLong(1)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572592475, 1),
                        "t" : NumberLong(1)
                },
                "lastAppliedWallTime" : ISODate("2019-11-01T07:14:35.324Z"),
                "lastDurableWallTime" : ISODate("2019-11-01T07:14:35.324Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572592445, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572592445, 1),
        "electionCandidateMetrics" : {
                "lastElectionReason" : "electionTimeout",
                "lastElectionDate" : ISODate("2019-11-01T07:05:04.871Z"),
                "termAtElection" : NumberLong(1),
                "lastCommittedOpTimeAtElection" : {
                        "ts" : Timestamp(0, 0),
                        "t" : NumberLong(-1)
                },
                "lastSeenOpTimeAtElection" : {
                        "ts" : Timestamp(1572591894, 1),
                        "t" : NumberLong(-1)
                },
                "numVotesNeeded" : 2,
                "priorityAtElection" : 1,
                "electionTimeoutMillis" : NumberLong(10000),
                "numCatchUpOps" : NumberLong(27017),
                "newTermStartDate" : ISODate("2019-11-01T07:05:05.307Z"),
                "wMajorityWriteAvailabilityDate" : ISODate("2019-11-01T07:05:05.990Z")
        },
        "members" : [
                {
                        "_id" : 0,
                        "name" : "m1:27017",
                        "ip" : "172.31.23.222",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 812,
                        "optime" : {
                                "ts" : Timestamp(1572592475, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:14:35Z"),
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572591904, 1),
                        "electionDate" : ISODate("2019-11-01T07:05:04Z"),
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                },
                {
                        "_id" : 1,
                        "name" : "m2:27017",
                        "ip" : "172.31.18.245",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 586,
                        "optime" : {
                                "ts" : Timestamp(1572592475, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572592475, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:14:35Z"),
                        "optimeDurableDate" : ISODate("2019-11-01T07:14:35Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:14:39.004Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:14:40.019Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "m1:27017",
                        "syncSourceHost" : "m1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1
                },
                {
                        "_id" : 2,
                        "name" : "m3:27017",
                        "ip" : "172.31.33.25",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 586,
                        "optime" : {
                                "ts" : Timestamp(1572592475, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572592475, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:14:35Z"),
                        "optimeDurableDate" : ISODate("2019-11-01T07:14:35Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:14:39.150Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:14:40.168Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "m1:27017",
                        "syncSourceHost" : "m1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572592475, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572592475, 1)
}
```
rs.config() before shutting machines:

{
        "_id" : "rs0",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "m1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "m2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "m3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5dbbd91653cbe1ff6c062bb3")
        }
}
Screenshot:
![ScreenShot](https://cdn1.savepice.ru/uploads/2019/11/1/1cfbf7f10ba4c2acf298ca27d23e3c06-full.png)


rs.status() after killing main machine:

{
        "set" : "rs0",
        "date" : ISODate("2019-11-01T07:26:32.330Z"),
        "myState" : 1,
        "term" : NumberLong(2),
        "syncingTo" : "",
        "syncSourceHost" : "",
        "syncSourceId" : -1,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572593191, 3),
                        "t" : NumberLong(2)
                },
                "lastCommittedWallTime" : ISODate("2019-11-01T07:26:31.720Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572593191, 3),
                        "t" : NumberLong(2)
                },
                "readConcernMajorityWallTime" : ISODate("2019-11-01T07:26:31.720Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572593191, 3),
                        "t" : NumberLong(2)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572593191, 3),
                        "t" : NumberLong(2)
                },
                "lastAppliedWallTime" : ISODate("2019-11-01T07:26:31.720Z"),
                "lastDurableWallTime" : ISODate("2019-11-01T07:26:31.720Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572593167, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572593167, 1),
        "electionCandidateMetrics" : {
                "lastElectionReason" : "stepUpRequestSkipDryRun",
                "lastElectionDate" : ISODate("2019-11-01T07:24:56.755Z"),
                "termAtElection" : NumberLong(2),
                "lastCommittedOpTimeAtElection" : {
                        "ts" : Timestamp(1572593095, 1),
                        "t" : NumberLong(1)
                },
                "lastSeenOpTimeAtElection" : {
                        "ts" : Timestamp(1572593095, 1),
                        "t" : NumberLong(1)
                },
                "numVotesNeeded" : 2,
                "priorityAtElection" : 1,
                "electionTimeoutMillis" : NumberLong(10000),
                "priorPrimaryMemberId" : 0,
                "numCatchUpOps" : NumberLong(419245120),
                "newTermStartDate" : ISODate("2019-11-01T07:24:57.346Z"),
                "wMajorityWriteAvailabilityDate" : ISODate("2019-11-01T07:24:58.469Z")
        },
        "members" : [
                {
                        "_id" : 0,
                        "name" : "m1:27017",
                        "ip" : "172.31.23.222",
                        "health" : 0,
                        "state" : 8,
                        "stateStr" : "(not reachable/healthy)",
                        "uptime" : 0,
                        "optime" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDate" : ISODate("1970-01-01T00:00:00Z"),
                        "optimeDurableDate" : ISODate("1970-01-01T00:00:00Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:26:30.823Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:24:57.036Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "Error connecting to m1:27017 (172.31.23.222:27017) :: caused by :: Connection refused",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "configVersion" : -1
                },
                {
                        "_id" : 1,
                        "name" : "m2:27017",
                        "ip" : "172.31.18.245",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 1502,
                        "optime" : {
                                "ts" : Timestamp(1572593191, 3),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:26:31Z"),
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572593096, 1),
                        "electionDate" : ISODate("2019-11-01T07:24:56Z"),
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                },
                {
                        "_id" : 2,
                        "name" : "m3:27017",
                        "ip" : "172.31.33.25",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 1297,
                        "optime" : {
                                "ts" : Timestamp(1572593187, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572593187, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:26:27Z"),
                        "optimeDurableDate" : ISODate("2019-11-01T07:26:27Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:26:30.806Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:26:30.511Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "m2:27017",
                        "syncSourceHost" : "m2:27017",
                        "syncSourceId" : 1,
                        "infoMessage" : "",
                        "configVersion" : 1
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572593191, 3),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572593191, 3)
}

rs.config() after killing main machine:


{
        "_id" : "rs0",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "m1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "m2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "m3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5dbbd91653cbe1ff6c062bb3")
        }
}

Screenshot:
![ScreenShot](https://cdn1.savepice.ru/uploads/2019/11/1/f9140e5bdc83670f206904c90a7d8b34-full.png)

