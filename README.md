# api documentation for  [kafka-node (v1.6.0)](https://github.com/SOHU-Co/kafka-node#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-kafka-node.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-kafka-node) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-kafka-node.svg)](https://travis-ci.org/npmdoc/node-npmdoc-kafka-node)
#### Client for Apache Kafka v0.8+

[![NPM](https://nodei.co/npm/kafka-node.png?downloads=true)](https://www.npmjs.com/package/kafka-node)

[![apidoc](https://npmdoc.github.io/node-npmdoc-kafka-node/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-kafka-node_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-kafka-node/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-kafka-node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-kafka-node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/SOHU-co/kafka-node/issues"
    },
    "dependencies": {
        "async": ">0.9 <2.0",
        "binary": "~0.3.0",
        "buffer-crc32": "~0.2.5",
        "buffermaker": "~1.2.0",
        "debug": "^2.1.3",
        "lodash": "^4.17.4",
        "minimatch": "^3.0.2",
        "nested-error-stacks": "^2.0.0",
        "node-zookeeper-client": "~0.2.2",
        "optional": "^0.1.3",
        "retry": "^0.10.1",
        "snappy": "^5.0.5",
        "uuid": "^3.0.0"
    },
    "description": "Client for Apache Kafka v0.8+",
    "devDependencies": {
        "coveralls": "^2.11.12",
        "doctoc": "^1.2.0",
        "eslint": "^3.7.0",
        "eslint-config-semistandard": "^7.0.0",
        "eslint-config-standard": "^6.2.0",
        "eslint-plugin-dependencies": "^1.3.0",
        "eslint-plugin-promise": "^3.4.0",
        "eslint-plugin-standard": "^2.0.1",
        "istanbul": "^0.4.4",
        "mocha": "^3.1.0",
        "nsp": "^2.6.2",
        "optimist": "^0.6.1",
        "proxyquire": "^1.7.10",
        "should": "^6.0.0",
        "sinon": "^1.17.2"
    },
    "directories": {},
    "dist": {
        "shasum": "c8c4b779610a45c53b7a5d177c20f63b46d36f87",
        "tarball": "https://registry.npmjs.org/kafka-node/-/kafka-node-1.6.0.tgz"
    },
    "engines": {
        "node": ">4.4.7"
    },
    "files": [
        "kafka.js",
        "logging.js",
        "lib"
    ],
    "gitHead": "a9f22e134f78dfc8aeeac8deee6331492dd7ceed",
    "homepage": "https://github.com/SOHU-Co/kafka-node#readme",
    "keywords": [
        "kafka",
        "zookeeper",
        "consumer",
        "producer",
        "broker"
    ],
    "license": "MIT",
    "main": "kafka.js",
    "maintainers": [
        {
            "name": "estliberitas",
            "email": "estliberitas@gmail.com"
        },
        {
            "name": "haio",
            "email": "mockingror@gmail.com"
        },
        {
            "name": "hyperlink",
            "email": "javascript@yahoo.com"
        }
    ],
    "name": "kafka-node",
    "optionalDependencies": {
        "snappy": "^5.0.5"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/SOHU-Co/kafka-node.git"
    },
    "scripts": {
        "startDocker": "./start-docker.sh",
        "stopDocker": "docker-compose down",
        "test": "eslint . && ./run-tests.sh && nsp check",
        "updateToc": "doctoc README.md --maxlevel 2 --notitle"
    },
    "version": "1.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module kafka-node](#apidoc.module.kafka-node)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Client (connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions)](#apidoc.element.kafka-node.Client)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Consumer (client, topics, options)](#apidoc.element.kafka-node.Consumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>ConsumerGroup (memberOptions, topics)](#apidoc.element.kafka-node.ConsumerGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>CustomPartitioner (partitioner)](#apidoc.element.kafka-node.CustomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>CyclicPartitioner ()](#apidoc.element.kafka-node.CyclicPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>DefaultPartitioner ()](#apidoc.element.kafka-node.DefaultPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelConsumer (client, topics, options)](#apidoc.element.kafka-node.HighLevelConsumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer (client, options, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer.super_ (client, options, defaultPartitionerType, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer.super_)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>KeyedMessage (key, value)](#apidoc.element.kafka-node.KeyedMessage)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>KeyedPartitioner ()](#apidoc.element.kafka-node.KeyedPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Offset (client)](#apidoc.element.kafka-node.Offset)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Producer (client, options, customPartitioner)](#apidoc.element.kafka-node.Producer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>RandomPartitioner ()](#apidoc.element.kafka-node.RandomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupMigrator (consumerGroup)](#apidoc.element.kafka-node.consumerGroupMigrator)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupRecovery (consumerGroup)](#apidoc.element.kafka-node.consumerGroupRecovery)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>logging (name)](#apidoc.element.kafka-node.logging)
1.  object <span class="apidocSignatureSpan">kafka-node.</span>Client.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>Consumer.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>ConsumerGroup.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>CyclicPartitioner.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>DefaultPartitioner.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>HighLevelConsumer.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer.super_.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>KeyedPartitioner.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>Offset.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>RandomPartitioner.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupMigrator.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupRecovery.prototype
1.  object <span class="apidocSignatureSpan">kafka-node.</span>partitioner
1.  object <span class="apidocSignatureSpan">kafka-node.</span>utils
1.  object <span class="apidocSignatureSpan">kafka-node.</span>zookeeper

#### [module kafka-node.Client](#apidoc.module.kafka-node.Client)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Client (connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions)](#apidoc.element.kafka-node.Client.Client)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.</span>super_ ()](#apidoc.element.kafka-node.Client.super_)

#### [module kafka-node.Client.prototype](#apidoc.module.kafka-node.Client.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>addTopics (topics, cb)](#apidoc.element.kafka-node.Client.prototype.addTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>brokerForLeader (leader, longpolling)](#apidoc.element.kafka-node.Client.prototype.brokerForLeader)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>checkMetadatas (payloads)](#apidoc.element.kafka-node.Client.prototype.checkMetadatas)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>clearCallbackQueue (socket, error)](#apidoc.element.kafka-node.Client.prototype.clearCallbackQueue)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>close (cb)](#apidoc.element.kafka-node.Client.prototype.close)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>closeBrokers (brokers)](#apidoc.element.kafka-node.Client.prototype.closeBrokers)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>connect ()](#apidoc.element.kafka-node.Client.prototype.connect)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>createBroker (host, port, longpolling)](#apidoc.element.kafka-node.Client.prototype.createBroker)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>createTopics (topics, isAsync, cb)](#apidoc.element.kafka-node.Client.prototype.createTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>getBrokers (longpolling)](#apidoc.element.kafka-node.Client.prototype.getBrokers)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>handleReceivedData (socket)](#apidoc.element.kafka-node.Client.prototype.handleReceivedData)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>hasMetadata (topic, partition)](#apidoc.element.kafka-node.Client.prototype.hasMetadata)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>leaderByPartition (topic, partition)](#apidoc.element.kafka-node.Client.prototype.leaderByPartition)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>loadMetadataForTopics (topics, cb)](#apidoc.element.kafka-node.Client.prototype.loadMetadataForTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>nextId ()](#apidoc.element.kafka-node.Client.prototype.nextId)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>nextSocketId ()](#apidoc.element.kafka-node.Client.prototype.nextSocketId)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>payloadsByLeader (payloads)](#apidoc.element.kafka-node.Client.prototype.payloadsByLeader)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>queueCallback (socket, id, data)](#apidoc.element.kafka-node.Client.prototype.queueCallback)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>reconnectBroker (oldSocket)](#apidoc.element.kafka-node.Client.prototype.reconnectBroker)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>refreshBrokers ()](#apidoc.element.kafka-node.Client.prototype.refreshBrokers)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>refreshMetadata (topicNames, cb)](#apidoc.element.kafka-node.Client.prototype.refreshMetadata)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>removeTopicMetadata (topics, cb)](#apidoc.element.kafka-node.Client.prototype.removeTopicMetadata)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>send (payloads, encoder, decoder, cb)](#apidoc.element.kafka-node.Client.prototype.send)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendFetchRequest (consumer, payloads, fetchMaxWaitMs, fetchMinBytes, maxTickMessages)](#apidoc.element.kafka-node.Client.prototype.sendFetchRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendGroupCoordinatorRequest (groupId, cb)](#apidoc.element.kafka-node.Client.prototype.sendGroupCoordinatorRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendGroupRequest (encode, decode, requestArgs)](#apidoc.element.kafka-node.Client.prototype.sendGroupRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendHeartbeatRequest (groupId, generationId, memberId, cb)](#apidoc.element.kafka-node.Client.prototype.sendHeartbeatRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendJoinGroupRequest (groupId, memberId, sessionTimeout, groupProtocol, cb)](#apidoc.element.kafka-node.Client.prototype.sendJoinGroupRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendLeaveGroupRequest (groupId, memberId, cb)](#apidoc.element.kafka-node.Client.prototype.sendLeaveGroupRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetCommitRequest (group, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetCommitRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetCommitV2Request (group, generationId, memberId, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetCommitV2Request)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetFetchRequest (group, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetFetchRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetFetchV1Request (group, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetFetchV1Request)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetRequest (payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendProduceRequest (payloads, requireAcks, ackTimeoutMs, cb)](#apidoc.element.kafka-node.Client.prototype.sendProduceRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendSyncGroupRequest (groupId, generationId, memberId, groupAssignment, cb)](#apidoc.element.kafka-node.Client.prototype.sendSyncGroupRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendToBroker (payloads, encoder, decoder, cb)](#apidoc.element.kafka-node.Client.prototype.sendToBroker)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>setupBroker (host, port, longpolling, brokers)](#apidoc.element.kafka-node.Client.prototype.setupBroker)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>setupBrokerProfiles (brokers)](#apidoc.element.kafka-node.Client.prototype.setupBrokerProfiles)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>topicExists (topics, cb)](#apidoc.element.kafka-node.Client.prototype.topicExists)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>unqueueCallback (socket, id)](#apidoc.element.kafka-node.Client.prototype.unqueueCallback)
1.  [function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>updateMetadatas (metadatas)](#apidoc.element.kafka-node.Client.prototype.updateMetadatas)

#### [module kafka-node.Consumer](#apidoc.module.kafka-node.Consumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Consumer (client, topics, options)](#apidoc.element.kafka-node.Consumer.Consumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.</span>super_ ()](#apidoc.element.kafka-node.Consumer.super_)

#### [module kafka-node.Consumer.prototype](#apidoc.module.kafka-node.Consumer.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>addTopics (topics, cb, fromOffset)](#apidoc.element.kafka-node.Consumer.prototype.addTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>autoCommit (force, cb)](#apidoc.element.kafka-node.Consumer.prototype.autoCommit)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>buildPayloads (payloads)](#apidoc.element.kafka-node.Consumer.prototype.buildPayloads)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>close (force, cb)](#apidoc.element.kafka-node.Consumer.prototype.close)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>commit (force, cb)](#apidoc.element.kafka-node.Consumer.prototype.commit)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>connect ()](#apidoc.element.kafka-node.Consumer.prototype.connect)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>fetch ()](#apidoc.element.kafka-node.Consumer.prototype.fetch)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>fetchOffset (payloads, cb)](#apidoc.element.kafka-node.Consumer.prototype.fetchOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>init ()](#apidoc.element.kafka-node.Consumer.prototype.init)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>pause ()](#apidoc.element.kafka-node.Consumer.prototype.pause)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>pauseTopics (topics)](#apidoc.element.kafka-node.Consumer.prototype.pauseTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>removeTopics (topics, cb)](#apidoc.element.kafka-node.Consumer.prototype.removeTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>resume ()](#apidoc.element.kafka-node.Consumer.prototype.resume)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>resumeTopics (topics)](#apidoc.element.kafka-node.Consumer.prototype.resumeTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>setOffset (topic, partition, offset)](#apidoc.element.kafka-node.Consumer.prototype.setOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>updateOffsets (topics, initing)](#apidoc.element.kafka-node.Consumer.prototype.updateOffsets)

#### [module kafka-node.ConsumerGroup](#apidoc.module.kafka-node.ConsumerGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>ConsumerGroup (memberOptions, topics)](#apidoc.element.kafka-node.ConsumerGroup.ConsumerGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.</span>super_ (client, topics, options)](#apidoc.element.kafka-node.ConsumerGroup.super_)

#### [module kafka-node.ConsumerGroup.prototype](#apidoc.module.kafka-node.ConsumerGroup.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>assignPartitions (protocol, groupMembers, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.assignPartitions)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>close (force, cb)](#apidoc.element.kafka-node.ConsumerGroup.prototype.close)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>connect ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.connect)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>fetchOffset (payloads, cb)](#apidoc.element.kafka-node.ConsumerGroup.prototype.fetchOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>getDefaultOffset (tp, defaultOffset)](#apidoc.element.kafka-node.ConsumerGroup.prototype.getDefaultOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>getOffset ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.getOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>handleJoinGroup (joinGroupResponse, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.handleJoinGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>handleSyncGroup (syncGroupResponse, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.handleSyncGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>leaveGroup (callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.leaveGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>saveDefaultOffsets (topicPartitionList, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.saveDefaultOffsets)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>scheduleReconnect (timeout)](#apidoc.element.kafka-node.ConsumerGroup.prototype.scheduleReconnect)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>sendHeartbeat ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.sendHeartbeat)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>sendOffsetCommitRequest (commits, cb)](#apidoc.element.kafka-node.ConsumerGroup.prototype.sendOffsetCommitRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>setCoordinatorId (coordinatorId)](#apidoc.element.kafka-node.ConsumerGroup.prototype.setCoordinatorId)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>setupProtocols (protocols)](#apidoc.element.kafka-node.ConsumerGroup.prototype.setupProtocols)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>startHeartbeats ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.startHeartbeats)
1.  [function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>stopHeartbeats ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.stopHeartbeats)

#### [module kafka-node.CustomPartitioner](#apidoc.module.kafka-node.CustomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>CustomPartitioner (partitioner)](#apidoc.element.kafka-node.CustomPartitioner.CustomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.CustomPartitioner.</span>super_ ()](#apidoc.element.kafka-node.CustomPartitioner.super_)

#### [module kafka-node.CyclicPartitioner](#apidoc.module.kafka-node.CyclicPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>CyclicPartitioner ()](#apidoc.element.kafka-node.CyclicPartitioner.CyclicPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.CyclicPartitioner.</span>super_ ()](#apidoc.element.kafka-node.CyclicPartitioner.super_)

#### [module kafka-node.CyclicPartitioner.prototype](#apidoc.module.kafka-node.CyclicPartitioner.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.CyclicPartitioner.prototype.</span>getPartition (partitions)](#apidoc.element.kafka-node.CyclicPartitioner.prototype.getPartition)

#### [module kafka-node.DefaultPartitioner](#apidoc.module.kafka-node.DefaultPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>DefaultPartitioner ()](#apidoc.element.kafka-node.DefaultPartitioner.DefaultPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.DefaultPartitioner.</span>super_ ()](#apidoc.element.kafka-node.DefaultPartitioner.super_)

#### [module kafka-node.DefaultPartitioner.prototype](#apidoc.module.kafka-node.DefaultPartitioner.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.DefaultPartitioner.prototype.</span>getPartition (partitions)](#apidoc.element.kafka-node.DefaultPartitioner.prototype.getPartition)

#### [module kafka-node.HighLevelConsumer](#apidoc.module.kafka-node.HighLevelConsumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelConsumer (client, topics, options)](#apidoc.element.kafka-node.HighLevelConsumer.HighLevelConsumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.</span>super_ ()](#apidoc.element.kafka-node.HighLevelConsumer.super_)

#### [module kafka-node.HighLevelConsumer.prototype](#apidoc.module.kafka-node.HighLevelConsumer.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>_releasePartitions (topicPayloads, callback)](#apidoc.element.kafka-node.HighLevelConsumer.prototype._releasePartitions)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>addTopics (topics, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.addTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>autoCommit (force, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.autoCommit)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>buildPayloads (payloads)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.buildPayloads)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>buildTopicPayloads (topics)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.buildTopicPayloads)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>close (force, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.close)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>commit (force, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.commit)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>connect ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.connect)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>fetch ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.fetch)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>fetchOffset (payloads, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.fetchOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>getTopicPayloads ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.getTopicPayloads)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>init ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.init)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>leaveGroup (cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.leaveGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>offsetRequest (payloads, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.offsetRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>pause ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.pause)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>rebalanceAttempt (oldTopicPayloads, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.rebalanceAttempt)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>registerConsumer (cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.registerConsumer)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>removeTopics (topics, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.removeTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>resume ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.resume)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>sendOffsetCommitRequest (commits, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.sendOffsetCommitRequest)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>setOffset (topic, partition, offset)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.setOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>stop (cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.stop)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>updateOffsets (topics, initing)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.updateOffsets)

#### [module kafka-node.HighLevelProducer](#apidoc.module.kafka-node.HighLevelProducer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer (client, options, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer.HighLevelProducer)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.</span>super_ (client, options, defaultPartitionerType, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer.super_)
1.  object <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.</span>PARTITIONER_TYPES

#### [module kafka-node.HighLevelProducer.super_](#apidoc.module.kafka-node.HighLevelProducer.super_)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.</span>super_ ()](#apidoc.element.kafka-node.HighLevelProducer.super_.super_)
1.  object <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.</span>PARTITIONER_TYPES

#### [module kafka-node.HighLevelProducer.super_.prototype](#apidoc.module.kafka-node.HighLevelProducer.super_.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>buildPayloads (payloads, topicMetadata)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.buildPayloads)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>close (cb)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.close)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>connect ()](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.connect)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>createTopics (topics, async, cb)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.createTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>send (payloads, cb)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.send)

#### [module kafka-node.KeyedPartitioner](#apidoc.module.kafka-node.KeyedPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>KeyedPartitioner ()](#apidoc.element.kafka-node.KeyedPartitioner.KeyedPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.KeyedPartitioner.</span>super_ ()](#apidoc.element.kafka-node.KeyedPartitioner.super_)

#### [module kafka-node.KeyedPartitioner.prototype](#apidoc.module.kafka-node.KeyedPartitioner.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.KeyedPartitioner.prototype.</span>getPartition (partitions, key)](#apidoc.element.kafka-node.KeyedPartitioner.prototype.getPartition)
1.  [function <span class="apidocSignatureSpan">kafka-node.KeyedPartitioner.prototype.</span>hashCode (string)](#apidoc.element.kafka-node.KeyedPartitioner.prototype.hashCode)

#### [module kafka-node.Offset](#apidoc.module.kafka-node.Offset)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Offset (client)](#apidoc.element.kafka-node.Offset.Offset)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.</span>super_ ()](#apidoc.element.kafka-node.Offset.super_)

#### [module kafka-node.Offset.prototype](#apidoc.module.kafka-node.Offset.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>buildPayloads (payloads)](#apidoc.element.kafka-node.Offset.prototype.buildPayloads)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>commit (groupId, payloads, cb)](#apidoc.element.kafka-node.Offset.prototype.commit)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetch (payloads, cb)](#apidoc.element.kafka-node.Offset.prototype.fetch)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetchCommits (groupId, payloads, cb)](#apidoc.element.kafka-node.Offset.prototype.fetchCommits)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetchEarliestOffsets (topics, cb)](#apidoc.element.kafka-node.Offset.prototype.fetchEarliestOffsets)
1.  [function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetchLatestOffsets (topics, cb)](#apidoc.element.kafka-node.Offset.prototype.fetchLatestOffsets)

#### [module kafka-node.Producer](#apidoc.module.kafka-node.Producer)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>Producer (client, options, customPartitioner)](#apidoc.element.kafka-node.Producer.Producer)
1.  [function <span class="apidocSignatureSpan">kafka-node.Producer.</span>super_ (client, options, defaultPartitionerType, customPartitioner)](#apidoc.element.kafka-node.Producer.super_)
1.  object <span class="apidocSignatureSpan">kafka-node.Producer.</span>PARTITIONER_TYPES

#### [module kafka-node.RandomPartitioner](#apidoc.module.kafka-node.RandomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>RandomPartitioner ()](#apidoc.element.kafka-node.RandomPartitioner.RandomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.RandomPartitioner.</span>super_ ()](#apidoc.element.kafka-node.RandomPartitioner.super_)

#### [module kafka-node.RandomPartitioner.prototype](#apidoc.module.kafka-node.RandomPartitioner.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.RandomPartitioner.prototype.</span>getPartition (partitions)](#apidoc.element.kafka-node.RandomPartitioner.prototype.getPartition)

#### [module kafka-node.consumerGroupMigrator](#apidoc.module.kafka-node.consumerGroupMigrator)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupMigrator (consumerGroup)](#apidoc.element.kafka-node.consumerGroupMigrator.consumerGroupMigrator)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.</span>super_ ()](#apidoc.element.kafka-node.consumerGroupMigrator.super_)

#### [module kafka-node.consumerGroupMigrator.prototype](#apidoc.module.kafka-node.consumerGroupMigrator.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>checkForOwners (topics, listenForChange)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.checkForOwners)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>checkForOwnersAndListenForChange (topics)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.checkForOwnersAndListenForChange)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>connectConsumerGroup ()](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.connectConsumerGroup)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>filterByExistingZkTopics (callback)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.filterByExistingZkTopics)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>getOffset (tp, defaultOffset)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.getOffset)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>saveHighLevelConsumerOffsets (topicPartitionList, callback)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.saveHighLevelConsumerOffsets)

#### [module kafka-node.consumerGroupRecovery](#apidoc.module.kafka-node.consumerGroupRecovery)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupRecovery (consumerGroup)](#apidoc.element.kafka-node.consumerGroupRecovery.consumerGroupRecovery)

#### [module kafka-node.consumerGroupRecovery.prototype](#apidoc.module.kafka-node.consumerGroupRecovery.prototype)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupRecovery.prototype.</span>clearError ()](#apidoc.element.kafka-node.consumerGroupRecovery.prototype.clearError)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupRecovery.prototype.</span>getRetryTimeout (error)](#apidoc.element.kafka-node.consumerGroupRecovery.prototype.getRetryTimeout)
1.  [function <span class="apidocSignatureSpan">kafka-node.consumerGroupRecovery.prototype.</span>tryToRecoverFrom (error, source)](#apidoc.element.kafka-node.consumerGroupRecovery.prototype.tryToRecoverFrom)

#### [module kafka-node.logging](#apidoc.module.kafka-node.logging)
1.  [function <span class="apidocSignatureSpan">kafka-node.</span>logging (name)](#apidoc.element.kafka-node.logging.logging)
1.  [function <span class="apidocSignatureSpan">kafka-node.logging.</span>setLoggerProvider (provider)](#apidoc.element.kafka-node.logging.setLoggerProvider)

#### [module kafka-node.partitioner](#apidoc.module.kafka-node.partitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>CustomPartitioner (partitioner)](#apidoc.element.kafka-node.partitioner.CustomPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>CyclicPartitioner ()](#apidoc.element.kafka-node.partitioner.CyclicPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>DefaultPartitioner ()](#apidoc.element.kafka-node.partitioner.DefaultPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>KeyedPartitioner ()](#apidoc.element.kafka-node.partitioner.KeyedPartitioner)
1.  [function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>RandomPartitioner ()](#apidoc.element.kafka-node.partitioner.RandomPartitioner)

#### [module kafka-node.utils](#apidoc.module.kafka-node.utils)
1.  [function <span class="apidocSignatureSpan">kafka-node.utils.</span>createTopicPartitionList (topicPartitions)](#apidoc.element.kafka-node.utils.createTopicPartitionList)
1.  [function <span class="apidocSignatureSpan">kafka-node.utils.</span>groupPartitionsByTopic (topicPartitions)](#apidoc.element.kafka-node.utils.groupPartitionsByTopic)
1.  [function <span class="apidocSignatureSpan">kafka-node.utils.</span>validateConfig (property, value)](#apidoc.element.kafka-node.utils.validateConfig)
1.  [function <span class="apidocSignatureSpan">kafka-node.utils.</span>validateTopicNames (topics)](#apidoc.element.kafka-node.utils.validateTopicNames)
1.  [function <span class="apidocSignatureSpan">kafka-node.utils.</span>validateTopics (topics)](#apidoc.element.kafka-node.utils.validateTopics)

#### [module kafka-node.zookeeper](#apidoc.module.kafka-node.zookeeper)
1.  [function <span class="apidocSignatureSpan">kafka-node.zookeeper.</span>Zookeeper (connectionString, options)](#apidoc.element.kafka-node.zookeeper.Zookeeper)
1.  [function <span class="apidocSignatureSpan">kafka-node.zookeeper.</span>ZookeeperConsumerMappings ()](#apidoc.element.kafka-node.zookeeper.ZookeeperConsumerMappings)



# <a name="apidoc.module.kafka-node"></a>[module kafka-node](#apidoc.module.kafka-node)

#### <a name="apidoc.element.kafka-node.Client"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Client (connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions)](#apidoc.element.kafka-node.Client)
- description and source-code
```javascript
Client = function (connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions) {
  if (this instanceof Client === false) {
    return new Client(connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions);
  }

  this.sslOptions = sslOptions;
  this.ssl = !!sslOptions;

  if (clientId) {
    validateConfig('clientId', clientId);
  }

  this.connectionString = connectionString || 'localhost:2181/';
  this.clientId = clientId || 'kafka-node-client';
  this.zkOptions = zkOptions;
  this.noAckBatchOptions = noAckBatchOptions;
  this.brokers = {};
  this.longpollingBrokers = {};
  this.topicMetadata = {};
  this.topicPartitions = {};
  this.correlationId = 0;
  this._socketId = 0;
  this.cbqueue = {};
  this.brokerMetadata = {};
  this.ready = false;
  this.connect();
}
```
- example usage
```shell
...
    partitionerType: 2
}
'''

''' js
var kafka = require('kafka-node'),
    Producer = kafka.Producer,
    client = new kafka.Client(),
    producer = new Producer(client);
'''

### Events

- 'ready': this event is emitted when producer is ready to send messages.
- 'error': this is the error event propagates from internal client, producer should always listen it.
...
```

#### <a name="apidoc.element.kafka-node.Consumer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Consumer (client, topics, options)](#apidoc.element.kafka-node.Consumer)
- description and source-code
```javascript
Consumer = function (client, topics, options) {
  if (!topics) {
    throw new Error('Must have payloads');
  }

  utils.validateTopics(topics);

  this.fetchCount = 0;
  this.client = client;
  this.options = _.defaults((options || {}), DEFAULTS);
  this.ready = false;
  this.paused = this.options.paused;
  this.id = nextId();
  this.payloads = this.buildPayloads(topics);
  this.connect();
  this.encoding = this.options.encoding;

  if (this.options.groupId) {
    utils.validateConfig('options.groupId', this.options.groupId);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>ConsumerGroup (memberOptions, topics)](#apidoc.element.kafka-node.ConsumerGroup)
- description and source-code
```javascript
function ConsumerGroup(memberOptions, topics) {
  EventEmitter.call(this);
  const self = this;
  this.options = _.defaults((memberOptions || {}), DEFAULTS);

  if (!this.options.heartbeatInterval) {
    this.options.heartbeatInterval = Math.floor(this.options.sessionTimeout / 3);
  }

  if (memberOptions.ssl === true) {
    memberOptions.ssl = {};
  }

  if (!(this.options.fromOffset in ACCEPTED_FROM_OFFSET)) {
    throw new Error('fromOffset ${this.options.fromOffset} should be either: ${Object.keys(ACCEPTED_FROM_OFFSET).join(', ')}');
  }

  if (!(this.options.outOfRangeOffset in ACCEPTED_FROM_OFFSET)) {
    throw new Error('outOfRangeOffset ${this.options.outOfRangeOffset} should be either: ${Object.keys(ACCEPTED_FROM_OFFSET).join
(', ')}');
  }

  this.client = new Client(memberOptions.host, memberOptions.id, memberOptions.zk,
    memberOptions.batch, memberOptions.ssl);

  if (_.isString(topics)) {
    topics = [topics];
  }

  assert(Array.isArray(topics), 'Array of topics is required');

  this.topics = topics;

  this.recovery = new ConsumerGroupRecovery(this);

  this.setupProtocols(this.options.protocol);

  if (this.options.connectOnReady && !this.options.migrateHLC) {
    this.client.once('ready', this.connect.bind(this));
  }

  if (this.options.migrateHLC) {
    const ConsumerGroupMigrator = require('./consumerGroupMigrator');
    this.migrator = new ConsumerGroupMigrator(this);
    this.migrator.on('error', function (error) {
      self.emit('error', error);
    });
  }

  this.client.on('error', function (err) {
    logger.error('Error from %s', self.client.clientId, err);
    self.emit('error', err);
  });

  const recoverFromBrokerChange = _.debounce(function () {
    logger.debug('brokersChanged refreshing metadata');
    self.client.refreshMetadata(self.topics, function (error) {
      if (error) {
        self.emit(error);
        return;
      }
      self.paused = false;
      if (!self.ready && !self.connecting) {
        if (self.reconnectTimer) {
          // brokers changed so bypass backoff retry and reconnect now
          clearTimeout(self.reconnectTimer);
          self.reconnectTimer = null;
        }
        self.connect();
      } else if (!self.connecting) {
        self.fetch();
      }
    });
  }, 200);

  this.client.on('brokersChanged', function () {
    self.pause();
    recoverFromBrokerChange();
  });

  this.client.on('reconnect', function (lastError) {
    self.fetch();
  });

  this.on('offsetOutOfRange', topic => {
    this.pause();
    if (this.options.outOfRangeOffset === 'none') {
      this.emit('error', new errors.InvalidConsumerOffsetError('Offset out of range for topic "${topic.topic}" partition ${topic
.partition}'));
      return;
    }

    topic.time = ACCEPTED_FROM_OFFSET[this.options.outOfRangeOffset];

    this.getOffset().fetch([topic], (error, result) => {
      if (error) {
        this.emit('error', new errors.InvalidConsumerOffsetError('Fetching ${this.options.outOfRangeOffset} offset failed', error
));
        return;
      }
      const offset = _.head(result[topic.topic][topic.partition]);
      const oldOffset = _.find(this.topicPayloads, {topic: topic.topic, partition: topic.partition}).offset;

      logger.debug('replacing %s-%s stale offset of %d with %d', topic.topic, topic.partition, oldOffset, offset);

      this.setOffset(topic.topic, topic.partition, offset);
      this.resume();
    });
  });

  // 'done' will be emit when a message fetch request complete
  this.on('done', function (topics) {
    self.updateOffsets(topics);
    if (!self.paused) {
      setImmediate(function () {
        self.fetch();
      });
    }
  });

  if (this.options.groupId) {
    validateConfig('options.groupId', this.options.groupId);
  }

  this.isLeader = false;
  this.coordinatorId = null;
  this.generationId = null;
  this.ready = false;
  this.topicPayloads = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.CustomPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>CustomPartitioner (partitioner)](#apidoc.element.kafka-node.CustomPartitioner)
- description and source-code
```javascript
CustomPartitioner = function (partitioner) {
  this.getPartition = partitioner;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.CyclicPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>CyclicPartitioner ()](#apidoc.element.kafka-node.CyclicPartitioner)
- description and source-code
```javascript
CyclicPartitioner = function () {
  this.c = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.DefaultPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>DefaultPartitioner ()](#apidoc.element.kafka-node.DefaultPartitioner)
- description and source-code
```javascript
DefaultPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelConsumer (client, topics, options)](#apidoc.element.kafka-node.HighLevelConsumer)
- description and source-code
```javascript
HighLevelConsumer = function (client, topics, options) {
  if (!topics) {
    throw new Error('Must have payloads');
  }
  this.fetchCount = 0;
  this.client = client;
  this.options = _.defaults((options || {}), DEFAULTS);
  this.initialised = false;
  this.ready = false;
  this.closing = false;
  this.paused = this.options.paused;
  this.rebalancing = false;
  this.pendingRebalances = 0;
  this.committing = false;
  this.needToCommit = false;
  this.id = this.options.id || this.options.groupId + '_' + uuid.v4();
  this.payloads = this.buildPayloads(topics);
  this.topicPayloads = this.buildTopicPayloads(topics);
  this.connect();

  if (this.options.groupId) {
    validateConfig('options.groupId', this.options.groupId);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer (client, options, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer)
- description and source-code
```javascript
function HighLevelProducer(client, options, customPartitioner) {
  BaseProducer.call(this, client, options, BaseProducer.PARTITIONER_TYPES.cyclic, customPartitioner);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer.super_ (client, options, defaultPartitionerType, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer.super_)
- description and source-code
```javascript
function BaseProducer(client, options, defaultPartitionerType, customPartitioner) {
  options = options || {};

  this.ready = false;
  this.client = client;

  this.requireAcks = options.requireAcks === undefined
    ? DEFAULTS.requireAcks
    : options.requireAcks;
  this.ackTimeoutMs = options.ackTimeoutMs === undefined
    ? DEFAULTS.ackTimeoutMs
    : options.ackTimeoutMs;

  if (customPartitioner !== undefined && options.partitionerType !== PARTITIONER_TYPES.custom) {
    throw new Error('Partitioner Type must be custom if providing a customPartitioner.');
  } else if (customPartitioner === undefined && options.partitionerType === PARTITIONER_TYPES.custom) {
    throw new Error('No customer partitioner defined');
  }

  var partitionerType = PARTITIONER_MAP[options.partitionerType] || PARTITIONER_MAP[defaultPartitionerType];

  // eslint-disable-next-line
  this.partitioner = new partitionerType(customPartitioner);

  this.connect();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.KeyedMessage"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>KeyedMessage (key, value)](#apidoc.element.kafka-node.KeyedMessage)
- description and source-code
```javascript
function KeyedMessage(key, value) {
  exports.Message.call(this, 0, 0, key, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.KeyedPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>KeyedPartitioner ()](#apidoc.element.kafka-node.KeyedPartitioner)
- description and source-code
```javascript
KeyedPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Offset"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Offset (client)](#apidoc.element.kafka-node.Offset)
- description and source-code
```javascript
Offset = function (client) {
  var self = this;
  this.client = client;
  this.ready = this.client.ready;
  this.client.on('ready', function () {
    self.ready = true;
    self.emit('ready');
  });
  this.client.once('connect', function () {
    self.emit('connect');
  });
  this.client.on('error', function (err) {
    self.emit('error', err);
  });
}
```
- example usage
```shell
...
* 'cb': *Function*, the callback

Example

'''js
var kafka = require('kafka-node'),
    client = new kafka.Client(),
    offset = new kafka.Offset(client);
    offset.fetch([
        { topic: 't', partition: 0, time: Date.now(), maxNum: 1 }
    ], function (err, data) {
        // data
        // { 't': { '0': [999] } }
    });
'''
...
```

#### <a name="apidoc.element.kafka-node.Producer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Producer (client, options, customPartitioner)](#apidoc.element.kafka-node.Producer)
- description and source-code
```javascript
function Producer(client, options, customPartitioner) {
  BaseProducer.call(this, client, options, BaseProducer.PARTITIONER_TYPES.default, customPartitioner);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.RandomPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>RandomPartitioner ()](#apidoc.element.kafka-node.RandomPartitioner)
- description and source-code
```javascript
RandomPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupMigrator (consumerGroup)](#apidoc.element.kafka-node.consumerGroupMigrator)
- description and source-code
```javascript
function ConsumerGroupMigrator(consumerGroup) {
  EventEmitter.call(this);
  assert(consumerGroup);
  const self = this;
  this.consumerGroup = consumerGroup;
  this.client = consumerGroup.client;
  var verified = 0;

  if (consumerGroup.options.migrateRolling) {
    this.zk = zookeeper.createClient(consumerGroup.client.connectionString, {retries: 10});
    this.zk.on('connected', function () {
      self.filterByExistingZkTopics(function (error, topics) {
        if (error) {
          return self.emit('error', error);
        }

        if (topics.length) {
          self.checkForOwnersAndListenForChange(topics);
        } else {
          logger.debug('No HLC topics exist in zookeeper.');
          self.connectConsumerGroup();
        }
      });
    });

    this.on('noOwnersForTopics', function (topics) {
      logger.debug('No owners for topics %s reported.', topics);
      if (++verified <= NUMER_OF_TIMES_TO_VERIFY) {
        logger.debug('%s verify %d of %d HLC has given up ownership by checking again in %d', self.client.clientId, verified,
          NUMER_OF_TIMES_TO_VERIFY, VERIFY_WAIT_TIME_MS);

        setTimeout(function () {
          self.checkForOwners(topics);
        }, VERIFY_WAIT_TIME_MS);
      } else {
        self.connectConsumerGroup();
      }
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.consumerGroupRecovery"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupRecovery (consumerGroup)](#apidoc.element.kafka-node.consumerGroupRecovery)
- description and source-code
```javascript
function ConsumerGroupRecovery(consumerGroup) {
  this.consumerGroup = consumerGroup;
  this.options = consumerGroup.options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.logging"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>logging (name)](#apidoc.element.kafka-node.logging)
- description and source-code
```javascript
function getLogger(name) {
  return loggerProvider(name);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.Client"></a>[module kafka-node.Client](#apidoc.module.kafka-node.Client)

#### <a name="apidoc.element.kafka-node.Client.Client"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Client (connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions)](#apidoc.element.kafka-node.Client.Client)
- description and source-code
```javascript
Client = function (connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions) {
  if (this instanceof Client === false) {
    return new Client(connectionString, clientId, zkOptions, noAckBatchOptions, sslOptions);
  }

  this.sslOptions = sslOptions;
  this.ssl = !!sslOptions;

  if (clientId) {
    validateConfig('clientId', clientId);
  }

  this.connectionString = connectionString || 'localhost:2181/';
  this.clientId = clientId || 'kafka-node-client';
  this.zkOptions = zkOptions;
  this.noAckBatchOptions = noAckBatchOptions;
  this.brokers = {};
  this.longpollingBrokers = {};
  this.topicMetadata = {};
  this.topicPartitions = {};
  this.correlationId = 0;
  this._socketId = 0;
  this.cbqueue = {};
  this.brokerMetadata = {};
  this.ready = false;
  this.connect();
}
```
- example usage
```shell
...
    partitionerType: 2
}
'''

''' js
var kafka = require('kafka-node'),
    Producer = kafka.Producer,
    client = new kafka.Client(),
    producer = new Producer(client);
'''

### Events

- 'ready': this event is emitted when producer is ready to send messages.
- 'error': this is the error event propagates from internal client, producer should always listen it.
...
```

#### <a name="apidoc.element.kafka-node.Client.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.</span>super_ ()](#apidoc.element.kafka-node.Client.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.Client.prototype"></a>[module kafka-node.Client.prototype](#apidoc.module.kafka-node.Client.prototype)

#### <a name="apidoc.element.kafka-node.Client.prototype.addTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>addTopics (topics, cb)](#apidoc.element.kafka-node.Client.prototype.addTopics)
- description and source-code
```javascript
addTopics = function (topics, cb) {
  var self = this;
  this.topicExists(topics, function (err) {
    if (err) return cb(err);
    self.loadMetadataForTopics(topics, function (err, resp) {
      if (err) return cb(err);
      self.updateMetadatas(resp);
      cb(null, topics);
    });
  });
}
```
- example usage
```shell
...
* 'topics': **Array**, array of topics to add
* 'cb': **Function**,the callback
* 'fromOffset': **Boolean**, if true, the consumer will fetch message from the specified offset, otherwise it will fetch message
 from the last commited offset of the topic.

Example:

''' js
consumer.addTopics(['t1', 't2'], function (err, added) {
});

or

consumer.addTopics([{ topic: 't1', offset: 10 }], function (err, added) {
}, true);
'''
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.brokerForLeader"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>brokerForLeader (leader, longpolling)](#apidoc.element.kafka-node.Client.prototype.brokerForLeader)
- description and source-code
```javascript
brokerForLeader = function (leader, longpolling) {
  var addr;
  var brokers = this.getBrokers(longpolling);
  // If leader is not give, choose the first broker as leader
  if (typeof leader === 'undefined') {
    if (!_.isEmpty(brokers)) {
      addr = Object.keys(brokers)[0];
      return brokers[addr];
    } else if (!_.isEmpty(this.brokerMetadata)) {
      leader = Object.keys(this.brokerMetadata)[0];
    } else {
      return;
    }
  }

  var broker = _.find(this.brokerProfiles, {id: leader});

  if (!broker) {
    return;
  }

  addr = broker.host + ':' + broker.port;

  return brokers[addr] || this.setupBroker(broker.host, broker.port, longpolling, brokers);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.checkMetadatas"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>checkMetadatas (payloads)](#apidoc.element.kafka-node.Client.prototype.checkMetadatas)
- description and source-code
```javascript
checkMetadatas = function (payloads) {
  if (_.isEmpty(this.topicMetadata)) return [ [], payloads ];
  // out: [ [metadata exists], [metadata not exists] ]
  var out = [ [], [] ];
  payloads.forEach(function (p) {
    if (this.hasMetadata(p.topic, p.partition)) out[0].push(p);
    else out[1].push(p);
  }.bind(this));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.clearCallbackQueue"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>clearCallbackQueue (socket, error)](#apidoc.element.kafka-node.Client.prototype.clearCallbackQueue)
- description and source-code
```javascript
clearCallbackQueue = function (socket, error) {
  var socketId = socket.socketId;
  var longpolling = socket.longpolling;

  if (!this.cbqueue.hasOwnProperty(socketId)) {
    return;
  }

  var queue = this.cbqueue[socketId];

  if (!longpolling) {
    Object.keys(queue).forEach(function (key) {
      var handlers = queue[key];
      var cb = handlers[1];
      cb(error);
    });
  }
  delete this.cbqueue[socketId];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.close"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>close (cb)](#apidoc.element.kafka-node.Client.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  this.closeBrokers(this.brokers);
  this.closeBrokers(this.longpollingBrokers);
  this.zk.close();
  cb && cb();
}
```
- example usage
```shell
...

### close(force, cb)
* 'force': **Boolean**, if set to true, it forces the consumer to commit the current offset before closing, default 'false'

Example

'''js
consumer.close(true, cb);
consumer.close(cb); //force is disabled
'''

## HighLevelConsumer
⚠️ ***This consumer has been deprecated in the latest version of Kafka (0.10.1) and is likely to be removed in the future. Please
 use the ConsumerGroup instead.***

### HighLevelConsumer(client, payloads, options)
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.closeBrokers"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>closeBrokers (brokers)](#apidoc.element.kafka-node.Client.prototype.closeBrokers)
- description and source-code
```javascript
closeBrokers = function (brokers) {
  _.each(brokers, function (broker) {
    broker.socket.closing = true;
    broker.socket.end();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.connect"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>connect ()](#apidoc.element.kafka-node.Client.prototype.connect)
- description and source-code
```javascript
connect = function () {
  var zk = this.zk = new Zookeeper(this.connectionString, this.zkOptions);
  var self = this;
  zk.once('init', function (brokers) {
    try {
      self.ready = true;
      self.brokerMetadata = brokers;
      self.setupBrokerProfiles(brokers);
      Object
          .keys(self.brokerProfiles)
          .some(function (key, index) {
            var broker = self.brokerProfiles[key];
            self.setupBroker(broker.host, broker.port, false, self.brokers);
            // Only connect one broker
            return !index;
          });
      self.emit('ready');
    } catch (error) {
      self.ready = false;
      self.emit('error', error);
    }
  });
  zk.on('brokersChanged', function (brokerMetadata) {
    try {
      self.brokerMetadata = brokerMetadata;
      logger.debug('brokersChanged', brokerMetadata);
      self.setupBrokerProfiles(brokerMetadata);
      self.refreshBrokers();
      // Emit after a 3 seconds
      setTimeout(function () {
        self.emit('brokersChanged');
      }, 3000);
    } catch (error) {
      self.emit('error', error);
    }
  });
  zk.once('disconnected', function () {
    if (!zk.closed) {
      zk.close();
      self.connect();
      self.emit('zkReconnect');
    }
  });
  zk.on('error', function (err) {
    self.emit('error', err);
  });
}
```
- example usage
```shell
...
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}

util.inherits(ConsumerGroupMigrator, EventEmitter);
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.createBroker"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>createBroker (host, port, longpolling)](#apidoc.element.kafka-node.Client.prototype.createBroker)
- description and source-code
```javascript
createBroker = function (host, port, longpolling) {
  var self = this;
  var socket;
  if (self.ssl) {
    socket = tls.connect(port, host, self.sslOptions);
  } else {
    socket = net.createConnection(port, host);
  }
  socket.addr = host + ':' + port;
  socket.host = host;
  socket.port = port;
  socket.socketId = this.nextSocketId();
  if (longpolling) socket.longpolling = true;

  socket.on('connect', function () {
    var lastError = this.error;
    this.error = null;
    if (lastError) {
      this.waiting = false;
      self.emit('reconnect');
    } else {
      self.emit('connect');
    }
  });
  socket.on('error', function (err) {
    this.error = err;
    self.emit('error', err);
  });
  socket.on('close', function (hadError) {
    self.emit('close', this);
    if (hadError && this.error) {
      self.clearCallbackQueue(this, this.error);
    } else {
      self.clearCallbackQueue(this, new errors.BrokerNotAvailableError('Broker not available'));
    }
    retry(this);
  });
  socket.on('end', function () {
    retry(this);
  });
  socket.buffer = new Buffer([]);
  socket.on('data', function (data) {
    this.buffer = Buffer.concat([this.buffer, data]);
    self.handleReceivedData(this);
  });
  socket.setKeepAlive(true, 60000);

  function retry (s) {
    if (s.retrying || s.closing) return;
    s.retrying = true;
    s.retryTimer = setTimeout(function () {
      if (s.closing) return;
      self.reconnectBroker(s);
    }, 1000);
  }
  return new BrokerWrapper(socket, this.noAckBatchOptions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.createTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>createTopics (topics, isAsync, cb)](#apidoc.element.kafka-node.Client.prototype.createTopics)
- description and source-code
```javascript
createTopics = function (topics, isAsync, cb) {
  topics = typeof topics === 'string' ? [topics] : topics;

  if (typeof isAsync === 'function' && typeof cb === 'undefined') {
    cb = isAsync;
    isAsync = true;
  }

  try {
    validateKafkaTopics(topics);
  } catch (e) {
    if (isAsync) return cb(e);
    throw e;
  }

  cb = _.once(cb);

  const getTopicsFromKafka = (topics, callback) => {
    this.loadMetadataForTopics(topics, function (error, resp) {
      if (error) {
        return callback(error);
      }
      callback(null, Object.keys(resp[1].metadata));
    });
  };

  const operation = retry.operation({ minTimeout: 200, maxTimeout: 2000 });

  operation.attempt(currentAttempt => {
    logger.debug('create topics currentAttempt', currentAttempt);
    getTopicsFromKafka(topics, function (error, kafkaTopics) {
      if (error) {
        if (operation.retry(error)) {
          return;
        }
      }

      logger.debug('kafka reported topics', kafkaTopics);
      const left = _.difference(topics, kafkaTopics);
      if (left.length === 0) {
        logger.debug('Topics created ${kafkaTopics}');
        return cb(null, kafkaTopics);
      }

      logger.debug('Topics left ${left.join(', ')}');
      if (!operation.retry(new Error('Topics not created ${left}'))) {
        cb(operation.mainError());
      }
    });
  });

  if (!isAsync) {
    cb(null);
  }
}
```
- example usage
```shell
...

''' js
var kafka = require('kafka-node'),
    Producer = kafka.Producer,
    client = new kafka.Client(),
    producer = new Producer(client);
// Create topics sync
producer.createTopics(['t','t1'], false, function (err, data) {
    console.log(data);
});
// Create topics async
producer.createTopics(['t'], true, function (err, data) {});
producer.createTopics(['t'], function (err, data) {});// Simply omit 2nd arg
'''
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.getBrokers"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>getBrokers (longpolling)](#apidoc.element.kafka-node.Client.prototype.getBrokers)
- description and source-code
```javascript
getBrokers = function (longpolling) {
  return longpolling ? this.longpollingBrokers : this.brokers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.handleReceivedData"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>handleReceivedData (socket)](#apidoc.element.kafka-node.Client.prototype.handleReceivedData)
- description and source-code
```javascript
handleReceivedData = function (socket) {
  var vars = Binary.parse(socket.buffer).word32bu('size').word32bu('correlationId').vars;
  var size = vars.size + 4;
  var correlationId = vars.correlationId;

  if (socket.buffer.length >= size) {
    var resp = socket.buffer.slice(0, size);
    var handlers = this.unqueueCallback(socket, correlationId);

    if (!handlers) return;
    var decoder = handlers[0];
    var cb = handlers[1];
    var result = decoder(resp);
    (result instanceof Error)
      ? cb.call(this, result)
      : cb.call(this, null, result);
    socket.buffer = socket.buffer.slice(size);
    if (socket.longpolling) socket.waiting = false;
  } else { return; }

  if (socket.buffer.length) {
    setImmediate(function () { this.handleReceivedData(socket); }.bind(this));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.hasMetadata"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>hasMetadata (topic, partition)](#apidoc.element.kafka-node.Client.prototype.hasMetadata)
- description and source-code
```javascript
hasMetadata = function (topic, partition) {
  var brokerMetadata = this.brokerMetadata;
  var leader = this.leaderByPartition(topic, partition);

  return (leader !== undefined) && brokerMetadata[leader];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.leaderByPartition"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>leaderByPartition (topic, partition)](#apidoc.element.kafka-node.Client.prototype.leaderByPartition)
- description and source-code
```javascript
leaderByPartition = function (topic, partition) {
  var topicMetadata = this.topicMetadata;
  return topicMetadata[topic] && topicMetadata[topic][partition] && topicMetadata[topic][partition].leader;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.loadMetadataForTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>loadMetadataForTopics (topics, cb)](#apidoc.element.kafka-node.Client.prototype.loadMetadataForTopics)
- description and source-code
```javascript
loadMetadataForTopics = function (topics, cb) {
  var correlationId = this.nextId();
  var request = protocol.encodeMetadataRequest(this.clientId, correlationId, topics);
  var broker = this.brokerForLeader();

  if (!broker || !broker.socket || broker.socket.error || broker.socket.destroyed) {
    return cb(new errors.BrokerNotAvailableError('Broker not available'));
  }

  this.queueCallback(broker.socket, correlationId, [protocol.decodeMetadataResponse, cb]);
  broker.write(request);
}
```
- example usage
```shell
...

## How do I get a list of all topics?

Call 'client.loadMetadataForTopics' with a blank topic array to get the entire list of available topics (and available brokers).

'''js
client.once('connect', function () {
	client.loadMetadataForTopics([], function (error, results) {
	  if (error) {
	  	return console.error(error);
	  }
	  console.log('%j', _.get(results, '1.metadata'));
	});
});
'''
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.nextId"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>nextId ()](#apidoc.element.kafka-node.Client.prototype.nextId)
- description and source-code
```javascript
nextId = function () {
  if (this.correlationId >= MAX_INT32) {
    this.correlationId = 0;
  }
  return this.correlationId++;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.nextSocketId"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>nextSocketId ()](#apidoc.element.kafka-node.Client.prototype.nextSocketId)
- description and source-code
```javascript
nextSocketId = function () {
  return this._socketId++;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.payloadsByLeader"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>payloadsByLeader (payloads)](#apidoc.element.kafka-node.Client.prototype.payloadsByLeader)
- description and source-code
```javascript
payloadsByLeader = function (payloads) {
  return payloads.reduce(function (out, p) {
    var leader = this.leaderByPartition(p.topic, p.partition);
    out[leader] = out[leader] || [];
    out[leader].push(p);
    return out;
  }.bind(this), {});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.queueCallback"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>queueCallback (socket, id, data)](#apidoc.element.kafka-node.Client.prototype.queueCallback)
- description and source-code
```javascript
queueCallback = function (socket, id, data) {
  var socketId = socket.socketId;
  var queue;

  if (this.cbqueue.hasOwnProperty(socketId)) {
    queue = this.cbqueue[socketId];
  } else {
    queue = {};
    this.cbqueue[socketId] = queue;
  }

  queue[id] = data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.reconnectBroker"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>reconnectBroker (oldSocket)](#apidoc.element.kafka-node.Client.prototype.reconnectBroker)
- description and source-code
```javascript
reconnectBroker = function (oldSocket) {
  oldSocket.retrying = false;
  if (oldSocket.error) {
    oldSocket.destroy();
  }
  var brokers = this.getBrokers(oldSocket.longpolling);
  var newBroker = this.setupBroker(oldSocket.host, oldSocket.port, oldSocket.longpolling, brokers);
  newBroker.socket.error = oldSocket.error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.refreshBrokers"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>refreshBrokers ()](#apidoc.element.kafka-node.Client.prototype.refreshBrokers)
- description and source-code
```javascript
refreshBrokers = function () {
  var self = this;
  var validBrokers = Object.keys(this.brokerProfiles);

  function closeDeadBrokers (brokers) {
    var deadBrokerKeys = _.difference(Object.keys(brokers), validBrokers);
    if (deadBrokerKeys.length) {
      self.closeBrokers(deadBrokerKeys.map(function (key) {
        var broker = brokers[key];
        delete brokers[key];
        return broker;
      }));
    }
  }

  closeDeadBrokers(this.brokers);
  closeDeadBrokers(this.longpollingBrokers);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.refreshMetadata"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>refreshMetadata (topicNames, cb)](#apidoc.element.kafka-node.Client.prototype.refreshMetadata)
- description and source-code
```javascript
refreshMetadata = function (topicNames, cb) {
  var self = this;
  if (!topicNames.length) return cb();
  attemptRequestMetadata(topicNames, cb);

  function attemptRequestMetadata (topics, cb) {
    var operation = retry.operation({ minTimeout: 200, maxTimeout: 1000 });
    operation.attempt(function (currentAttempt) {
      logger.debug('refresh metadata currentAttempt', currentAttempt);
      self.loadMetadataForTopics(topics, function (err, resp) {
        err = err || resp[1].error;
        if (operation.retry(err)) {
          return;
        }
        if (err) {
          logger.debug('refresh metadata error', err.message);
          return cb(err);
        }
        self.updateMetadatas(resp);
        cb();
      });
    });
  }
}
```
- example usage
```shell
...

Error:

'''
BrokerNotAvailableError: Could not find the leader
'''

Call 'client.refreshMetadata()' before sending the first message. Reference issue [#354](https://github.com/SOHU-Co/kafka-node/issues
/354)



## How do I debug an issue?
This module uses the [debug module](https://github.com/visionmedia/debug) so you can just run below before starting your app.

'''bash
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.removeTopicMetadata"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>removeTopicMetadata (topics, cb)](#apidoc.element.kafka-node.Client.prototype.removeTopicMetadata)
- description and source-code
```javascript
removeTopicMetadata = function (topics, cb) {
  topics.forEach(function (t) {
    if (this.topicMetadata[t]) delete this.topicMetadata[t];
  }.bind(this));
  cb(null, topics.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.send"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>send (payloads, encoder, decoder, cb)](#apidoc.element.kafka-node.Client.prototype.send)
- description and source-code
```javascript
send = function (payloads, encoder, decoder, cb) {
  var self = this;
  var _payloads = payloads;
  // payloads: [ [metadata exists], [metadata not exists] ]
  payloads = this.checkMetadatas(payloads);
  if (payloads[0].length && !payloads[1].length) {
    this.sendToBroker(_.flatten(payloads), encoder, decoder, cb);
    return;
  }
  if (payloads[1].length) {
    var topicNames = payloads[1].map(function (p) { return p.topic; });
    this.loadMetadataForTopics(topicNames, function (err, resp) {
      if (err) {
        return cb(err);
      }

      var error = resp[1].error;
      if (error) {
        return cb(error);
      }

      self.updateMetadatas(resp);
      // check payloads again
      payloads = self.checkMetadatas(_payloads);
      if (payloads[1].length) {
        return cb(new errors.BrokerNotAvailableError('Could not find the leader'));
      }

      self.sendToBroker(payloads[1].concat(payloads[0]), encoder, decoder, cb);
    });
  }
}
```
- example usage
```shell
...
    producer = new Producer(client),
    km = new KeyedMessage('key', 'message'),
    payloads = [
        { topic: 'topic1', messages: 'hi', partition: 0 },
        { topic: 'topic2', messages: ['hello', 'world', km] }
    ];
producer.on('ready', function () {
    producer.send(payloads, function (err, data) {
        console.log(data);
    });
});

producer.on('error', function (err) {})
'''
> ⚠️**WARNING**: Batch multiple messages of the same topic/partition together as an array on the 'messages' attribute otherwise
you may lose messages!
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendFetchRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendFetchRequest (consumer, payloads, fetchMaxWaitMs, fetchMinBytes, maxTickMessages)](#apidoc.element.kafka-node.Client.prototype.sendFetchRequest)
- description and source-code
```javascript
sendFetchRequest = function (consumer, payloads, fetchMaxWaitMs, fetchMinBytes, maxTickMessages) {
  var self = this;
  var encoder = protocol.encodeFetchRequest(fetchMaxWaitMs, fetchMinBytes);
  var decoder = protocol.decodeFetchResponse(function (err, type, message) {
    if (err) {
      if (err.message === 'OffsetOutOfRange') {
        return consumer.emit('offsetOutOfRange', err);
      } else if (err.message === 'NotLeaderForPartition' || err.message === 'UnknownTopicOrPartition') {
        return self.emit('brokersChanged');
      }

      return consumer.emit('error', err);
    }

    var encoding = consumer.options.encoding;

    if (type === 'message') {
      if (encoding !== 'buffer' && message.value) {
        message.value = message.value.toString(encoding);
      }

      consumer.emit('message', message);
    } else {
      consumer.emit('done', message);
    }
  }, maxTickMessages);

  this.send(payloads, encoder, decoder, function (err) {
    if (err) {
      Array.prototype.unshift.call(arguments, 'error');
      consumer.emit.apply(consumer, arguments);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendGroupCoordinatorRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendGroupCoordinatorRequest (groupId, cb)](#apidoc.element.kafka-node.Client.prototype.sendGroupCoordinatorRequest)
- description and source-code
```javascript
sendGroupCoordinatorRequest = function (groupId, cb) {
  this.sendGroupRequest(protocol.encodeGroupCoordinatorRequest, protocol.decodeGroupCoordinatorResponse, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendGroupRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendGroupRequest (encode, decode, requestArgs)](#apidoc.element.kafka-node.Client.prototype.sendGroupRequest)
- description and source-code
```javascript
sendGroupRequest = function (encode, decode, requestArgs) {
  requestArgs = _.values(requestArgs);
  var cb = requestArgs.pop();
  var correlationId = this.nextId();

  requestArgs.unshift(this.clientId, correlationId);

  var request = encode.apply(null, requestArgs);
  var broker = this.brokerForLeader(this.coordinatorId);

  if (!broker || !broker.socket || broker.socket.error || broker.socket.destroyed) {
    return cb(new errors.BrokerNotAvailableError('Broker not available'));
  }

  this.queueCallback(broker.socket, correlationId, [decode, cb]);
  broker.write(request);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendHeartbeatRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendHeartbeatRequest (groupId, generationId, memberId, cb)](#apidoc.element.kafka-node.Client.prototype.sendHeartbeatRequest)
- description and source-code
```javascript
sendHeartbeatRequest = function (groupId, generationId, memberId, cb) {
  this.sendGroupRequest(protocol.encodeGroupHeartbeat, protocol.decodeGroupHeartbeat, arguments);
}
```
- example usage
```shell
...
constructor (client, handler) {
  this.client = client;
  this.handler = handler;
  this.pending = true;
}

send (groupId, generationId, memberId) {
  this.client.sendHeartbeatRequest(groupId, generationId, memberId, (error) => {
    if (this.canceled) {
      logger.debug('heartbeat yielded after being canceled', error);
      return;
    }
    this.pending = false;
    this.handler(error);
  });
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendJoinGroupRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendJoinGroupRequest (groupId, memberId, sessionTimeout, groupProtocol, cb)](#apidoc.element.kafka-node.Client.prototype.sendJoinGroupRequest)
- description and source-code
```javascript
sendJoinGroupRequest = function (groupId, memberId, sessionTimeout, groupProtocol, cb) {
  this.sendGroupRequest(protocol.encodeJoinGroupRequest, protocol.decodeJoinGroupResponse, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendLeaveGroupRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendLeaveGroupRequest (groupId, memberId, cb)](#apidoc.element.kafka-node.Client.prototype.sendLeaveGroupRequest)
- description and source-code
```javascript
sendLeaveGroupRequest = function (groupId, memberId, cb) {
  this.sendGroupRequest(protocol.encodeLeaveGroupRequest, protocol.decodeLeaveGroupResponse, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendOffsetCommitRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetCommitRequest (group, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetCommitRequest)
- description and source-code
```javascript
sendOffsetCommitRequest = function (group, payloads, cb) {
  var encoder = protocol.encodeOffsetCommitRequest(group);
  var decoder = protocol.decodeOffsetCommitResponse;
  this.send(payloads, encoder, decoder, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendOffsetCommitV2Request"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetCommitV2Request (group, generationId, memberId, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetCommitV2Request)
- description and source-code
```javascript
sendOffsetCommitV2Request = function (group, generationId, memberId, payloads, cb) {
  var encoder = protocol.encodeOffsetCommitV2Request;
  var decoder = protocol.decodeOffsetCommitResponse;
  this.sendGroupRequest(encoder, decoder, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendOffsetFetchRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetFetchRequest (group, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetFetchRequest)
- description and source-code
```javascript
sendOffsetFetchRequest = function (group, payloads, cb) {
  var encoder = protocol.encodeOffsetFetchRequest(group);
  var decoder = protocol.decodeOffsetFetchResponse;
  this.send(payloads, encoder, decoder, cb);
}
```
- example usage
```shell
...
    }
  }
);
};

ConsumerGroupMigrator.prototype.saveHighLevelConsumerOffsets = function (topicPartitionList, callback) {
const self = this;
this.client.sendOffsetFetchRequest(this.consumerGroup.options.groupId, topicPartitionList, function (error, results) {
  logger.debug('sendOffsetFetchRequest response:', results, error);
  if (error) {
    return callback(error);
  }
  self.offsets = results;
  callback(null);
});
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendOffsetFetchV1Request"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetFetchV1Request (group, payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetFetchV1Request)
- description and source-code
```javascript
sendOffsetFetchV1Request = function (group, payloads, cb) {
  var encoder = protocol.encodeOffsetFetchV1Request;
  var decoder = protocol.decodeOffsetFetchV1Response;
  this.sendGroupRequest(encoder, decoder, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendOffsetRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendOffsetRequest (payloads, cb)](#apidoc.element.kafka-node.Client.prototype.sendOffsetRequest)
- description and source-code
```javascript
sendOffsetRequest = function (payloads, cb) {
  var encoder = protocol.encodeOffsetRequest;
  var decoder = protocol.decodeOffsetResponse;
  this.send(payloads, encoder, decoder, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendProduceRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendProduceRequest (payloads, requireAcks, ackTimeoutMs, cb)](#apidoc.element.kafka-node.Client.prototype.sendProduceRequest)
- description and source-code
```javascript
sendProduceRequest = function (payloads, requireAcks, ackTimeoutMs, cb) {
  var encoder = protocol.encodeProduceRequest(requireAcks, ackTimeoutMs);
  var decoder = protocol.decodeProduceResponse;
  var self = this;

  decoder.requireAcks = requireAcks;

  async.each(payloads, buildRequest, function (err) {
    if (err) return cb(err);
    self.send(payloads, encoder, decoder, function (err, result) {
      if (err) {
        if (err.message === 'NotLeaderForPartition') {
          self.emit('brokersChanged');
        }
        cb(err);
      } else {
        cb(null, result);
      }
    });
  });

  function buildRequest (payload, cb) {
    var attributes = payload.attributes;
    var codec = getCodec(attributes);

    if (!codec) return cb();

    var innerSet = encodeMessageSet(payload.messages);
    codec.encode(innerSet, function (err, message) {
      if (err) return cb(err);
      payload.messages = [ new Message(0, attributes, '', message) ];
      cb();
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendSyncGroupRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendSyncGroupRequest (groupId, generationId, memberId, groupAssignment, cb)](#apidoc.element.kafka-node.Client.prototype.sendSyncGroupRequest)
- description and source-code
```javascript
sendSyncGroupRequest = function (groupId, generationId, memberId, groupAssignment, cb) {
  this.sendGroupRequest(protocol.encodeSyncGroupRequest, protocol.decodeSyncGroupResponse, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.sendToBroker"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>sendToBroker (payloads, encoder, decoder, cb)](#apidoc.element.kafka-node.Client.prototype.sendToBroker)
- description and source-code
```javascript
sendToBroker = function (payloads, encoder, decoder, cb) {
  var longpolling = encoder.name === 'encodeFetchRequest';
  payloads = this.payloadsByLeader(payloads);
  if (!longpolling) {
    cb = wrap(payloads, cb);
  }
  for (var leader in payloads) {
    if (!payloads.hasOwnProperty(leader)) {
      continue;
    }
    var correlationId = this.nextId();
    var request = encoder(this.clientId, correlationId, payloads[leader]);
    var broker = this.brokerForLeader(leader, longpolling);
    if (!broker || !broker.socket || broker.socket.error || broker.socket.closing || broker.socket.destroyed) {
      return cb(new errors.BrokerNotAvailableError('Could not find the leader'), payloads[leader]);
    }

    if (longpolling) {
      if (broker.socket.waiting) continue;
      broker.socket.waiting = true;
    }

    if (decoder.requireAcks === 0) {
      broker.writeAsync(request);
      cb(null, { result: 'no ack' });
    } else {
      this.queueCallback(broker.socket, correlationId, [decoder, cb]);
      broker.write(request);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.setupBroker"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>setupBroker (host, port, longpolling, brokers)](#apidoc.element.kafka-node.Client.prototype.setupBroker)
- description and source-code
```javascript
setupBroker = function (host, port, longpolling, brokers) {
  var brokerKey = host + ':' + port;
  brokers[brokerKey] = this.createBroker(host, port, longpolling);
  return brokers[brokerKey];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.setupBrokerProfiles"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>setupBrokerProfiles (brokers)](#apidoc.element.kafka-node.Client.prototype.setupBrokerProfiles)
- description and source-code
```javascript
setupBrokerProfiles = function (brokers) {
  this.brokerProfiles = Object.create(null);
  var self = this;
  var protocol = self.ssl ? 'ssl:' : 'plaintext:';

  Object.keys(brokers).forEach(function (key) {
    var brokerProfile = brokers[key];
    var addr;

    if (brokerProfile.endpoints && brokerProfile.endpoints.length) {
      var endpoint = _.find(brokerProfile.endpoints, function (endpoint) {
        return url.parse(endpoint).protocol === protocol;
      });

      if (endpoint == null) {
        throw new Error(['No kafka endpoint found for broker: ', key, ' with protocol ', protocol].join(''));
      }

      var endpointUrl = url.parse(endpoint);

      addr = endpointUrl.hostname + ':' + endpointUrl.port;

      brokerProfile.host = endpointUrl.hostname;
      brokerProfile.port = endpointUrl.port;
    } else {
      addr = brokerProfile.host + ':' + brokerProfile.port;
    }
    assert(brokerProfile.host && brokerProfile.port, 'kafka host or port is empty');

    self.brokerProfiles[addr] = brokerProfile;
    self.brokerProfiles[addr].id = key;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.topicExists"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>topicExists (topics, cb)](#apidoc.element.kafka-node.Client.prototype.topicExists)
- description and source-code
```javascript
topicExists = function (topics, cb) {
  var notExistsTopics = [];
  var self = this;

  async.each(topics, checkZK, function (err) {
    if (err) return cb(err);
    if (notExistsTopics.length) return cb(new errors.TopicsNotExistError(notExistsTopics));
    cb();
  });

  function checkZK (topic, cb) {
    self.zk.topicExists(topic, function (err, existed, topic) {
      if (err) return cb(err);
      if (!existed) notExistsTopics.push(topic);
      cb();
    });
  }
}
```
- example usage
```shell
...
var path = '/brokers/topics/' + topic;
var self = this;
this.client.exists(
  path,
  function (event) {
    logger.debug('Got event: %s.', event);
    if (watch) {
      self.topicExists(topic, cb);
    }
  },
  function (error, stat) {
    if (error) return cb(error);
    cb(null, !!stat, topic);
  }
);
...
```

#### <a name="apidoc.element.kafka-node.Client.prototype.unqueueCallback"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>unqueueCallback (socket, id)](#apidoc.element.kafka-node.Client.prototype.unqueueCallback)
- description and source-code
```javascript
unqueueCallback = function (socket, id) {
  var socketId = socket.socketId;

  if (!this.cbqueue.hasOwnProperty(socketId)) {
    return null;
  }

  var queue = this.cbqueue[socketId];
  if (!queue.hasOwnProperty(id)) {
    return null;
  }

  var result = queue[id];

  // cleanup socket queue
  delete queue[id];
  if (!Object.keys(queue).length) {
    delete this.cbqueue[socketId];
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Client.prototype.updateMetadatas"></a>[function <span class="apidocSignatureSpan">kafka-node.Client.prototype.</span>updateMetadatas (metadatas)](#apidoc.element.kafka-node.Client.prototype.updateMetadatas)
- description and source-code
```javascript
updateMetadatas = function (metadatas) {
  // _.extend(this.brokerMetadata, metadatas[0])
  _.extend(this.topicMetadata, metadatas[1].metadata);
  for (var topic in this.topicMetadata) {
    if (!this.topicMetadata.hasOwnProperty(topic)) {
      continue;
    }
    this.topicPartitions[topic] = Object.keys(this.topicMetadata[topic]).map(function (val) {
      return parseInt(val, 10);
    });
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.Consumer"></a>[module kafka-node.Consumer](#apidoc.module.kafka-node.Consumer)

#### <a name="apidoc.element.kafka-node.Consumer.Consumer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Consumer (client, topics, options)](#apidoc.element.kafka-node.Consumer.Consumer)
- description and source-code
```javascript
Consumer = function (client, topics, options) {
  if (!topics) {
    throw new Error('Must have payloads');
  }

  utils.validateTopics(topics);

  this.fetchCount = 0;
  this.client = client;
  this.options = _.defaults((options || {}), DEFAULTS);
  this.ready = false;
  this.paused = this.options.paused;
  this.id = nextId();
  this.payloads = this.buildPayloads(topics);
  this.connect();
  this.encoding = this.options.encoding;

  if (this.options.groupId) {
    utils.validateConfig('options.groupId', this.options.groupId);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.</span>super_ ()](#apidoc.element.kafka-node.Consumer.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.Consumer.prototype"></a>[module kafka-node.Consumer.prototype](#apidoc.module.kafka-node.Consumer.prototype)

#### <a name="apidoc.element.kafka-node.Consumer.prototype.addTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>addTopics (topics, cb, fromOffset)](#apidoc.element.kafka-node.Consumer.prototype.addTopics)
- description and source-code
```javascript
addTopics = function (topics, cb, fromOffset) {
  fromOffset = !!fromOffset;
  var self = this;
  if (!this.ready) {
    setTimeout(function () {
      self.addTopics(topics, cb, fromOffset);
    }
    , 100);
    return;
  }

  // The default is that the topics is a string array of topic names
  var topicNames = topics;

  // If the topics is actually an object and not string we assume it is an array of payloads
  if (typeof topics[0] === 'object') {
    topicNames = topics.map(function (p) { return p.topic; });
  }

  this.client.addTopics(
    topicNames,
    function (err, added) {
      if (err) return cb && cb(err, added);

      var payloads = self.buildPayloads(topics);
      var reFetch = !self.payloads.length;

      if (fromOffset) {
        payloads.forEach(function (p) {
          self.payloads.push(p);
        });
        if (reFetch) self.fetch();
        cb && cb(null, added);
        return;
      }

      // update offset of topics that will be added
      self.fetchOffset(payloads, function (err, offsets) {
        if (err) return cb(err);
        payloads.forEach(function (p) {
          var offset = offsets[p.topic][p.partition];
          if (offset === -1) offset = 0;
          p.offset = offset;
          self.payloads.push(p);
        });
        if (reFetch) self.fetch();
        cb && cb(null, added);
      });
    }
  );
}
```
- example usage
```shell
...
* 'topics': **Array**, array of topics to add
* 'cb': **Function**,the callback
* 'fromOffset': **Boolean**, if true, the consumer will fetch message from the specified offset, otherwise it will fetch message
 from the last commited offset of the topic.

Example:

''' js
consumer.addTopics(['t1', 't2'], function (err, added) {
});

or

consumer.addTopics([{ topic: 't1', offset: 10 }], function (err, added) {
}, true);
'''
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.autoCommit"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>autoCommit (force, cb)](#apidoc.element.kafka-node.Consumer.prototype.autoCommit)
- description and source-code
```javascript
function autoCommit(force, cb) {
  if (arguments.length === 1) {
    cb = force;
    force = false;
  }

  if (this.committing && !force) return cb(null, 'Offset committing');

  this.committing = true;
  setTimeout(function () {
    this.committing = false;
  }.bind(this), this.options.autoCommitIntervalMs);

  var payloads = this.payloads;
  if (this.pausedPayloads) payloads = payloads.concat(this.pausedPayloads);

  var commits = payloads.filter(function (p) { return p.offset !== 0; });
  if (commits.length) {
    this.client.sendOffsetCommitRequest(this.options.groupId, commits, cb);
  } else {
    cb(null, 'Nothing to be committed');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.buildPayloads"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>buildPayloads (payloads)](#apidoc.element.kafka-node.Consumer.prototype.buildPayloads)
- description and source-code
```javascript
buildPayloads = function (payloads) {
  var self = this;
  return payloads.map(function (p) {
    if (typeof p !== 'object') p = { topic: p };
    p.partition = p.partition || 0;
    p.offset = p.offset || 0;
    p.maxBytes = self.options.fetchMaxBytes;
    p.metadata = 'm'; // metadata can be arbitrary
    return p;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.close"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>close (force, cb)](#apidoc.element.kafka-node.Consumer.prototype.close)
- description and source-code
```javascript
close = function (force, cb) {
  this.ready = false;
  if (typeof force === 'function') {
    cb = force;
    force = false;
  }

  if (force) {
    this.commit(force, function (err) {
      if (err) {
        return cb(err);
      }
      this.client.close(cb);
    }.bind(this));
  } else {
    this.client.close(cb);
  }
}
```
- example usage
```shell
...

### close(force, cb)
* 'force': **Boolean**, if set to true, it forces the consumer to commit the current offset before closing, default 'false'

Example

'''js
consumer.close(true, cb);
consumer.close(cb); //force is disabled
'''

## HighLevelConsumer
⚠️ ***This consumer has been deprecated in the latest version of Kafka (0.10.1) and is likely to be removed in the future. Please
 use the ConsumerGroup instead.***

### HighLevelConsumer(client, payloads, options)
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.commit"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>commit (force, cb)](#apidoc.element.kafka-node.Consumer.prototype.commit)
- description and source-code
```javascript
function autoCommit(force, cb) {
  if (arguments.length === 1) {
    cb = force;
    force = false;
  }

  if (this.committing && !force) return cb(null, 'Offset committing');

  this.committing = true;
  setTimeout(function () {
    this.committing = false;
  }.bind(this), this.options.autoCommitIntervalMs);

  var payloads = this.payloads;
  if (this.pausedPayloads) payloads = payloads.concat(this.pausedPayloads);

  var commits = payloads.filter(function (p) { return p.offset !== 0; });
  if (commits.length) {
    this.client.sendOffsetCommitRequest(this.options.groupId, commits, cb);
  } else {
    cb(null, 'Nothing to be committed');
  }
}
```
- example usage
```shell
...
Commit offset of the current topics manually, this method should be called when a consumer leaves

* 'cb': **Function**, the callback

Example:

''' js
consumer.commit(function(err, data) {
});
'''

### setOffset(topic, partition, offset)
Set offset of the given topic

* 'topic': **String**
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.connect"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>connect ()](#apidoc.element.kafka-node.Consumer.prototype.connect)
- description and source-code
```javascript
connect = function () {
  var self = this;
  // Client already exists
  this.ready = this.client.ready;
  if (this.ready) this.init();

  this.client.on('ready', function () {
    logger.debug('consumer ready');
    if (!self.ready) self.init();
    self.ready = true;
  });

  this.client.on('error', function (err) {
    logger.error('client error %s', err.message);
    self.emit('error', err);
  });

  this.client.on('close', function () {
    logger.debug('connection closed');
  });

  this.client.on('brokersChanged', function () {
    var topicNames = self.payloads.map(function (p) {
      return p.topic;
    });

    this.refreshMetadata(topicNames, function (err) {
      if (err) return self.emit('error', err);
      self.fetch();
    });
  });
  // 'done' will be emit when a message fetch request complete
  this.on('done', function (topics) {
    self.updateOffsets(topics);
    setImmediate(function () {
      self.fetch();
    });
  });
}
```
- example usage
```shell
...
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}

util.inherits(ConsumerGroupMigrator, EventEmitter);
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.fetch"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>fetch ()](#apidoc.element.kafka-node.Consumer.prototype.fetch)
- description and source-code
```javascript
fetch = function () {
  if (!this.ready || this.paused) return;
  this.client.sendFetchRequest(this, this.payloads, this.options.fetchMaxWaitMs, this.options.fetchMinBytes);
}
```
- example usage
```shell
...

Example

'''js
var kafka = require('kafka-node'),
    client = new kafka.Client(),
    offset = new kafka.Offset(client);
    offset.fetch([
        { topic: 't', partition: 0, time: Date.now(), maxNum: 1 }
    ], function (err, data) {
        // data
        // { 't': { '0': [999] } }
    });
'''
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.fetchOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>fetchOffset (payloads, cb)](#apidoc.element.kafka-node.Consumer.prototype.fetchOffset)
- description and source-code
```javascript
fetchOffset = function (payloads, cb) {
  this.client.sendOffsetFetchRequest(this.options.groupId, payloads, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.init"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>init ()](#apidoc.element.kafka-node.Consumer.prototype.init)
- description and source-code
```javascript
init = function () {
  if (!this.payloads.length) {
    return;
  }

  var self = this;
  var topics = self.payloads.map(function (p) { return p.topic; });

  self.client.topicExists(topics, function (err) {
    if (err) {
      return self.emit('error', err);
    }

    if (self.options.fromOffset) {
      return self.fetch();
    }

    self.fetchOffset(self.payloads, function (err, topics) {
      if (err) {
        return self.emit('error', err);
      }

      self.updateOffsets(topics, true);
      self.fetch();
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.pause"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>pause ()](#apidoc.element.kafka-node.Consumer.prototype.pause)
- description and source-code
```javascript
pause = function () {
  this.paused = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.pauseTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>pauseTopics (topics)](#apidoc.element.kafka-node.Consumer.prototype.pauseTopics)
- description and source-code
```javascript
pauseTopics = function (topics) {
  if (!this.pausedPayloads) this.pausedPayloads = [];
  pauseOrResume(this.payloads, this.pausedPayloads, topics);
}
```
- example usage
```shell
...
### resume()
Resume the consumer. Resumes the fetch loop.

### pauseTopics(topics)
Pause specify topics

'''
consumer.pauseTopics([
    'topic1',
    { topic: 'topic2', partition: 0 }
]);
'''

### resumeTopics(topics)
Resume specify topics
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.removeTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>removeTopics (topics, cb)](#apidoc.element.kafka-node.Consumer.prototype.removeTopics)
- description and source-code
```javascript
removeTopics = function (topics, cb) {
  topics = typeof topics === 'string' ? [topics] : topics;
  this.payloads = this.payloads.filter(function (p) {
    return !~topics.indexOf(p.topic);
  });

  this.client.removeTopicMetadata(topics, cb);
}
```
- example usage
```shell
...
### removeTopics(topics, cb)
* 'topics': **Array**, array of topics to remove
* 'cb': **Function**, the callback

Example:

''' js
consumer.removeTopics(['t1', 't2'], function (err, removed) {
});
'''

### commit(cb)
Commit offset of the current topics manually, this method should be called when a consumer leaves

* 'cb': **Function**, the callback
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.resume"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>resume ()](#apidoc.element.kafka-node.Consumer.prototype.resume)
- description and source-code
```javascript
resume = function () {
  this.paused = false;
  this.fetch();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.resumeTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>resumeTopics (topics)](#apidoc.element.kafka-node.Consumer.prototype.resumeTopics)
- description and source-code
```javascript
resumeTopics = function (topics) {
  if (!this.pausedPayloads) this.pausedPayloads = [];
  var reFetch = !this.payloads.length;
  pauseOrResume(this.pausedPayloads, this.payloads, topics);
  reFetch = reFetch && this.payloads.length;
  if (reFetch) this.fetch();
}
```
- example usage
```shell
...
]);
'''

### resumeTopics(topics)
Resume specify topics

'''
consumer.resumeTopics([
    'topic1',
    { topic: 'topic2', partition: 0 }
]);
'''

### close(force, cb)
* 'force': **Boolean**, if set to true, it forces the consumer to commit the current offset before closing, default 'false'
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.setOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>setOffset (topic, partition, offset)](#apidoc.element.kafka-node.Consumer.prototype.setOffset)
- description and source-code
```javascript
setOffset = function (topic, partition, offset) {
  this.payloads.every(function (p) {
    if (p.topic === topic && p.partition == partition) { // eslint-disable-line eqeqeq
      p.offset = offset;
      return false;
    }
    return true;
  });
}
```
- example usage
```shell
...
* 'partition': **Number**

* 'offset': **Number**

Example:

''' js
consumer.setOffset('topic', 0, 0);
'''

### pause()
Pause the consumer. ***Calling 'pause' does not automatically stop messages from being emitted.*** This is because pause just stops
 the kafka consumer fetch loop. Each iteration of the fetch loop can obtain a batch of messages (limited by 'fetchMaxBytes').

### resume()
Resume the consumer. Resumes the fetch loop.
...
```

#### <a name="apidoc.element.kafka-node.Consumer.prototype.updateOffsets"></a>[function <span class="apidocSignatureSpan">kafka-node.Consumer.prototype.</span>updateOffsets (topics, initing)](#apidoc.element.kafka-node.Consumer.prototype.updateOffsets)
- description and source-code
```javascript
updateOffsets = function (topics, initing) {
  this.payloads.forEach(function (p) {
    if (!_.isEmpty(topics[p.topic]) && topics[p.topic][p.partition] !== undefined) {
      var offset = topics[p.topic][p.partition];
      if (offset === -1) offset = 0;
      if (!initing) p.offset = offset + 1;
      else p.offset = offset;
    }
  });

  if (this.options.autoCommit && !initing) {
    this.autoCommit(false, function (err) {
      err && logger.debug('auto commit offset', err);
    });
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.ConsumerGroup"></a>[module kafka-node.ConsumerGroup](#apidoc.module.kafka-node.ConsumerGroup)

#### <a name="apidoc.element.kafka-node.ConsumerGroup.ConsumerGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>ConsumerGroup (memberOptions, topics)](#apidoc.element.kafka-node.ConsumerGroup.ConsumerGroup)
- description and source-code
```javascript
function ConsumerGroup(memberOptions, topics) {
  EventEmitter.call(this);
  const self = this;
  this.options = _.defaults((memberOptions || {}), DEFAULTS);

  if (!this.options.heartbeatInterval) {
    this.options.heartbeatInterval = Math.floor(this.options.sessionTimeout / 3);
  }

  if (memberOptions.ssl === true) {
    memberOptions.ssl = {};
  }

  if (!(this.options.fromOffset in ACCEPTED_FROM_OFFSET)) {
    throw new Error('fromOffset ${this.options.fromOffset} should be either: ${Object.keys(ACCEPTED_FROM_OFFSET).join(', ')}');
  }

  if (!(this.options.outOfRangeOffset in ACCEPTED_FROM_OFFSET)) {
    throw new Error('outOfRangeOffset ${this.options.outOfRangeOffset} should be either: ${Object.keys(ACCEPTED_FROM_OFFSET).join
(', ')}');
  }

  this.client = new Client(memberOptions.host, memberOptions.id, memberOptions.zk,
    memberOptions.batch, memberOptions.ssl);

  if (_.isString(topics)) {
    topics = [topics];
  }

  assert(Array.isArray(topics), 'Array of topics is required');

  this.topics = topics;

  this.recovery = new ConsumerGroupRecovery(this);

  this.setupProtocols(this.options.protocol);

  if (this.options.connectOnReady && !this.options.migrateHLC) {
    this.client.once('ready', this.connect.bind(this));
  }

  if (this.options.migrateHLC) {
    const ConsumerGroupMigrator = require('./consumerGroupMigrator');
    this.migrator = new ConsumerGroupMigrator(this);
    this.migrator.on('error', function (error) {
      self.emit('error', error);
    });
  }

  this.client.on('error', function (err) {
    logger.error('Error from %s', self.client.clientId, err);
    self.emit('error', err);
  });

  const recoverFromBrokerChange = _.debounce(function () {
    logger.debug('brokersChanged refreshing metadata');
    self.client.refreshMetadata(self.topics, function (error) {
      if (error) {
        self.emit(error);
        return;
      }
      self.paused = false;
      if (!self.ready && !self.connecting) {
        if (self.reconnectTimer) {
          // brokers changed so bypass backoff retry and reconnect now
          clearTimeout(self.reconnectTimer);
          self.reconnectTimer = null;
        }
        self.connect();
      } else if (!self.connecting) {
        self.fetch();
      }
    });
  }, 200);

  this.client.on('brokersChanged', function () {
    self.pause();
    recoverFromBrokerChange();
  });

  this.client.on('reconnect', function (lastError) {
    self.fetch();
  });

  this.on('offsetOutOfRange', topic => {
    this.pause();
    if (this.options.outOfRangeOffset === 'none') {
      this.emit('error', new errors.InvalidConsumerOffsetError('Offset out of range for topic "${topic.topic}" partition ${topic
.partition}'));
      return;
    }

    topic.time = ACCEPTED_FROM_OFFSET[this.options.outOfRangeOffset];

    this.getOffset().fetch([topic], (error, result) => {
      if (error) {
        this.emit('error', new errors.InvalidConsumerOffsetError('Fetching ${this.options.outOfRangeOffset} offset failed', error
));
        return;
      }
      const offset = _.head(result[topic.topic][topic.partition]);
      const oldOffset = _.find(this.topicPayloads, {topic: topic.topic, partition: topic.partition}).offset;

      logger.debug('replacing %s-%s stale offset of %d with %d', topic.topic, topic.partition, oldOffset, offset);

      this.setOffset(topic.topic, topic.partition, offset);
      this.resume();
    });
  });

  // 'done' will be emit when a message fetch request complete
  this.on('done', function (topics) {
    self.updateOffsets(topics);
    if (!self.paused) {
      setImmediate(function () {
        self.fetch();
      });
    }
  });

  if (this.options.groupId) {
    validateConfig('options.groupId', this.options.groupId);
  }

  this.isLeader = false;
  this.coordinatorId = null;
  this.generationId = null;
  this.ready = false;
  this.topicPayloads = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.</span>super_ (client, topics, options)](#apidoc.element.kafka-node.ConsumerGroup.super_)
- description and source-code
```javascript
super_ = function (client, topics, options) {
  if (!topics) {
    throw new Error('Must have payloads');
  }
  this.fetchCount = 0;
  this.client = client;
  this.options = _.defaults((options || {}), DEFAULTS);
  this.initialised = false;
  this.ready = false;
  this.closing = false;
  this.paused = this.options.paused;
  this.rebalancing = false;
  this.pendingRebalances = 0;
  this.committing = false;
  this.needToCommit = false;
  this.id = this.options.id || this.options.groupId + '_' + uuid.v4();
  this.payloads = this.buildPayloads(topics);
  this.topicPayloads = this.buildTopicPayloads(topics);
  this.connect();

  if (this.options.groupId) {
    validateConfig('options.groupId', this.options.groupId);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.ConsumerGroup.prototype"></a>[module kafka-node.ConsumerGroup.prototype](#apidoc.module.kafka-node.ConsumerGroup.prototype)

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.assignPartitions"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>assignPartitions (protocol, groupMembers, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.assignPartitions)
- description and source-code
```javascript
assignPartitions = function (protocol, groupMembers, callback) {
  logger.debug('Assigning Partitions to members', groupMembers);
  logger.debug('Using group protocol', protocol);

  protocol = _.find(this.protocols, {name: protocol});

  var self = this;
  var topics = _(groupMembers).map('subscription').flatten().uniq().value();

  async.waterfall([
    function (callback) {
      logger.debug('loadingMetadata for topics:', topics);
      self.client.loadMetadataForTopics(topics, callback);
    },

    function (metadataResponse, callback) {
      var metadata = mapTopicToPartitions(metadataResponse[1].metadata);
      logger.debug('mapTopicToPartitions', metadata);
      protocol.assign(metadata, groupMembers, callback);
    }
  ], callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.close"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>close (force, cb)](#apidoc.element.kafka-node.ConsumerGroup.prototype.close)
- description and source-code
```javascript
close = function (force, cb) {
  var self = this;
  this.ready = false;

  this.stopHeartbeats();

  if (typeof force === 'function') {
    cb = force;
    force = false;
  }

  async.series([
    function (callback) {
      if (force) {
        self.commit(true, callback);
        return;
      }
      callback(null);
    },
    function (callback) {
      self.leaveGroup(function (error) {
        if (error) {
          logger.error('Leave group failed with', error);
        }
        callback(null);
      });
    },
    function (callback) {
      self.client.close(callback);
    }
  ], cb);
}
```
- example usage
```shell
...

### close(force, cb)
* 'force': **Boolean**, if set to true, it forces the consumer to commit the current offset before closing, default 'false'

Example

'''js
consumer.close(true, cb);
consumer.close(cb); //force is disabled
'''

## HighLevelConsumer
⚠️ ***This consumer has been deprecated in the latest version of Kafka (0.10.1) and is likely to be removed in the future. Please
 use the ConsumerGroup instead.***

### HighLevelConsumer(client, payloads, options)
...
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.connect"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>connect ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.connect)
- description and source-code
```javascript
connect = function () {
  if (this.connecting) {
    logger.warn('Connect ignored. Currently connecting.');
    return;
  }

  logger.debug('Connecting %s', this.client.clientId);
  var self = this;

  this.connecting = true;
  this.emit('rebalancing');

  async.waterfall([
    function (callback) {
      if (self.client.coordinatorId) {
        return callback(null, null);
      }
      self.client.sendGroupCoordinatorRequest(self.options.groupId, callback);
    },

    function (coordinatorInfo, callback) {
      logger.debug('GroupCoordinator Response:', coordinatorInfo);
      if (coordinatorInfo) {
        self.setCoordinatorId(coordinatorInfo.coordinatorId);
      }
      self.client.sendJoinGroupRequest(self.options.groupId, emptyStrIfNull(self.memberId), self.options.sessionTimeout, self.protocols
, callback);
    },

    function (joinGroupResponse, callback) {
      self.handleJoinGroup(joinGroupResponse, callback);
    },

    function (groupAssignment, callback) {
      logger.debug('SyncGroup Request from %s', self.memberId);
      self.client.sendSyncGroupRequest(self.options.groupId, self.generationId, self.memberId, groupAssignment, callback);
    },

    function (syncGroupResponse, callback) {
      self.handleSyncGroup(syncGroupResponse, callback);
    }
  ], function (error, startFetch) {
    self.connecting = false;
    self.rebalancing = false;
    if (error) {
      return self.recovery.tryToRecoverFrom(error, 'connect');
    }

    self.ready = true;
    self.recovery.clearError();

    logger.debug('generationId', self.generationId);

    if (startFetch) {
      self.fetch();
    }
    self.startHeartbeats();
    self.emit('connect');
    self.emit('rebalanced');
  });
}
```
- example usage
```shell
...
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}

util.inherits(ConsumerGroupMigrator, EventEmitter);
...
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.fetchOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>fetchOffset (payloads, cb)](#apidoc.element.kafka-node.ConsumerGroup.prototype.fetchOffset)
- description and source-code
```javascript
fetchOffset = function (payloads, cb) {
  this.client.sendOffsetFetchV1Request(this.options.groupId, payloads, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.getDefaultOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>getDefaultOffset (tp, defaultOffset)](#apidoc.element.kafka-node.ConsumerGroup.prototype.getDefaultOffset)
- description and source-code
```javascript
getDefaultOffset = function (tp, defaultOffset) {
  return _.get(this.defaultOffsets, [tp.topic, tp.partition], defaultOffset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.getOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>getOffset ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.getOffset)
- description and source-code
```javascript
getOffset = function () {
  if (this.offset) {
    return this.offset;
  }
  this.offset = new Offset(this.client);
  // we can ignore this since we are already forwarding error event emitted from client
  this.offset.on('error', _.noop);
  return this.offset;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.handleJoinGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>handleJoinGroup (joinGroupResponse, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.handleJoinGroup)
- description and source-code
```javascript
handleJoinGroup = function (joinGroupResponse, callback) {
  logger.debug('joinGroupResponse %j from %s', joinGroupResponse, this.client.clientId);

  this.isLeader = (joinGroupResponse.leaderId === joinGroupResponse.memberId);
  this.generationId = joinGroupResponse.generationId;
  this.memberId = joinGroupResponse.memberId;

  var groupAssignment;
  if (this.isLeader) {
    // assign partitions
    return this.assignPartitions(joinGroupResponse.groupProtocol, joinGroupResponse.members, callback);
  }
  callback(null, groupAssignment);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.handleSyncGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>handleSyncGroup (syncGroupResponse, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.handleSyncGroup)
- description and source-code
```javascript
handleSyncGroup = function (syncGroupResponse, callback) {
  logger.debug('SyncGroup Response');
  var self = this;
  var ownedTopics = Object.keys(syncGroupResponse.partitions);
  if (ownedTopics.length) {
    logger.debug('%s owns topics: ', self.client.clientId, syncGroupResponse.partitions);

    const topicPartitionList = createTopicPartitionList(syncGroupResponse.partitions);
    const useDefaultOffsets = self.options.fromOffset in ACCEPTED_FROM_OFFSET;

    async.waterfall([
      function (callback) {
        self.fetchOffset(syncGroupResponse.partitions, callback);
      },
      function (offsets, callback) {
        logger.debug('%s fetchOffset Response: %j', self.client.clientId, offsets);

        var noOffset = topicPartitionList.some(function (tp) {
          return offsets[tp.topic][tp.partition] === -1;
        });

        if (noOffset) {
          logger.debug('No saved offsets');

          if (self.options.fromOffset === 'none') {
            return callback(new Error('${self.client.clientId} owns topics and partitions which contains no saved offsets for group
 '${self.options.groupId}''));
          }

          async.parallel([
            function (callback) {
              if (self.migrator) {
                return self.migrator.saveHighLevelConsumerOffsets(topicPartitionList, callback);
              }
              callback(null);
            },
            function (callback) {
              if (useDefaultOffsets) {
                return self.saveDefaultOffsets(topicPartitionList, callback);
              }
              callback(null);
            }
          ], function (error) {
            if (error) {
              return callback(error);
            }
            logger.debug('%s defaultOffset Response for %s: %j', self.client.clientId, self.options.fromOffset, self.defaultOffsets
);
            callback(null, offsets);
          });
        } else {
          logger.debug('Has saved offsets');
          callback(null, offsets);
        }
      },
      function (offsets, callback) {
        self.topicPayloads = self.buildPayloads(topicPartitionList).map(function (p) {
          var offset = offsets[p.topic][p.partition];
          if (offset === -1) { // -1 means no offset was saved for this topic/partition combo
            offset = useDefaultOffsets ? self.getDefaultOffset(p, 0) : 0;
            if (self.migrator) {
              offset = self.migrator.getOffset(p, offset);
            }
          }
          p.offset = offset;
          return p;
        });
        callback(null, true);
      }
    ], callback);
  } else { // no partitions assigned
    callback(null, false);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.leaveGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>leaveGroup (callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.leaveGroup)
- description and source-code
```javascript
leaveGroup = function (callback) {
  logger.debug('%s leaving group', this.client.clientId);
  var self = this;
  this.stopHeartbeats();
  if (self.generationId != null && self.memberId) {
    this.client.sendLeaveGroupRequest(this.options.groupId, this.memberId, function (error) {
      self.generationId = null;
      callback(error);
    });
  } else {
    callback(null);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.saveDefaultOffsets"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>saveDefaultOffsets (topicPartitionList, callback)](#apidoc.element.kafka-node.ConsumerGroup.prototype.saveDefaultOffsets)
- description and source-code
```javascript
saveDefaultOffsets = function (topicPartitionList, callback) {
  var self = this;
  const offsetPayload = _(topicPartitionList).cloneDeep().map(tp => {
    tp.time = ACCEPTED_FROM_OFFSET[this.options.fromOffset];
    return tp;
  });

  self.getOffset().fetch(offsetPayload, function (error, result) {
    if (error) {
      return callback(error);
    }
    self.defaultOffsets = _.mapValues(result, function (partitionOffsets) {
      return _.mapValues(partitionOffsets, _.head);
    });
    callback(null);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.scheduleReconnect"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>scheduleReconnect (timeout)](#apidoc.element.kafka-node.ConsumerGroup.prototype.scheduleReconnect)
- description and source-code
```javascript
scheduleReconnect = function (timeout) {
  assert(timeout);
  this.rebalancing = true;

  if (this.reconnectTimer) {
    clearTimeout(this.reconnectTimer);
  }

  var self = this;
  this.reconnectTimer = setTimeout(function () {
    self.reconnectTimer = null;
    self.connect();
  }, timeout);
}
```
- example usage
```shell
...

  if (retry) {
    retryTimeout = this.getRetryTimeout(error);
  }

  if (retry && retryTimeout) {
    logger.debug('RECOVERY from %s: %s retrying in %s ms', source, this.consumerGroup.client.clientId, retryTimeout, error);
    this.consumerGroup.scheduleReconnect(retryTimeout);
  } else {
    this.consumerGroup.emit('error', error);
  }
  this.lastError = error;
};

ConsumerGroupRecovery.prototype.clearError = function () {
...
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.sendHeartbeat"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>sendHeartbeat ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.sendHeartbeat)
- description and source-code
```javascript
sendHeartbeat = function () {
  assert(this.memberId, 'invalid memberId');
  assert(this.generationId >= 0, 'invalid generationId');
  // logger.debug('%s ❤️  ->', this.client.clientId);
  var self = this;

  function heartbeatCallback (error) {
    if (error) {
      logger.warn('%s Heartbeat error:', self.client.clientId, error);
      self.recovery.tryToRecoverFrom(error, 'heartbeat');
    }
    // logger.debug('%s 💚 <-', self.client.clientId, error);
  }

  const heartbeat = new Heartbeat(this.client, heartbeatCallback);
  heartbeat.send(this.options.groupId, this.generationId, this.memberId);

  return heartbeat;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.sendOffsetCommitRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>sendOffsetCommitRequest (commits, cb)](#apidoc.element.kafka-node.ConsumerGroup.prototype.sendOffsetCommitRequest)
- description and source-code
```javascript
sendOffsetCommitRequest = function (commits, cb) {
  if (this.generationId && this.memberId) {
    this.client.sendOffsetCommitV2Request(this.options.groupId, this.generationId, this.memberId, commits, cb);
  } else {
    cb(null, 'Nothing to be committed');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.setCoordinatorId"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>setCoordinatorId (coordinatorId)](#apidoc.element.kafka-node.ConsumerGroup.prototype.setCoordinatorId)
- description and source-code
```javascript
setCoordinatorId = function (coordinatorId) {
  this.client.coordinatorId = String(coordinatorId);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.setupProtocols"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>setupProtocols (protocols)](#apidoc.element.kafka-node.ConsumerGroup.prototype.setupProtocols)
- description and source-code
```javascript
setupProtocols = function (protocols) {
  if (!Array.isArray(protocols)) {
    protocols = [protocols];
  }

  this.protocols = protocols.map(function (protocol) {
    if (typeof protocol === 'string') {
      if (!(protocol in builtInProtocols)) {
        throw new Error('Unknown built in assignment protocol ' + protocol);
      }
      protocol = _.assign({}, builtInProtocols[protocol]);
    } else {
      checkProtocol(protocol);
    }

    protocol.subscription = this.topics;
    return protocol;
  }, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.startHeartbeats"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>startHeartbeats ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.startHeartbeats)
- description and source-code
```javascript
startHeartbeats = function () {
  assert(this.options.sessionTimeout > 0);
  assert(this.ready, 'consumerGroup is not ready');

  const heartbeatIntervalMs = this.options.heartbeatInterval || (Math.floor(this.options.sessionTimeout / 3));

  logger.debug('%s started heartbeats at every %d ms', this.client.clientId, heartbeatIntervalMs);
  this.stopHeartbeats();

  let heartbeat = this.sendHeartbeat();

  this.heartbeatInterval = setInterval(() => {
    // only send another heartbeat if we got a response from the last one
    if (heartbeat.verifyResolved()) {
      heartbeat = this.sendHeartbeat();
    }
  }, heartbeatIntervalMs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.ConsumerGroup.prototype.stopHeartbeats"></a>[function <span class="apidocSignatureSpan">kafka-node.ConsumerGroup.prototype.</span>stopHeartbeats ()](#apidoc.element.kafka-node.ConsumerGroup.prototype.stopHeartbeats)
- description and source-code
```javascript
stopHeartbeats = function () {
  this.heartbeatInterval && clearInterval(this.heartbeatInterval);
}
```
- example usage
```shell
...
function ConsumerGroupRecovery (consumerGroup) {
this.consumerGroup = consumerGroup;
this.options = consumerGroup.options;
}

ConsumerGroupRecovery.prototype.tryToRecoverFrom = function (error, source) {
this.consumerGroup.ready = false;
this.consumerGroup.stopHeartbeats();

var retryTimeout = false;
var retry = recoverableErrors.some(function (recoverableItem) {
  if (isErrorInstanceOf(error, recoverableItem.errors)) {
    recoverableItem.handler && recoverableItem.handler.call(this.consumerGroup, error);
    return true;
  }
...
```



# <a name="apidoc.module.kafka-node.CustomPartitioner"></a>[module kafka-node.CustomPartitioner](#apidoc.module.kafka-node.CustomPartitioner)

#### <a name="apidoc.element.kafka-node.CustomPartitioner.CustomPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>CustomPartitioner (partitioner)](#apidoc.element.kafka-node.CustomPartitioner.CustomPartitioner)
- description and source-code
```javascript
CustomPartitioner = function (partitioner) {
  this.getPartition = partitioner;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.CustomPartitioner.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.CustomPartitioner.</span>super_ ()](#apidoc.element.kafka-node.CustomPartitioner.super_)
- description and source-code
```javascript
super_ = function () {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.CyclicPartitioner"></a>[module kafka-node.CyclicPartitioner](#apidoc.module.kafka-node.CyclicPartitioner)

#### <a name="apidoc.element.kafka-node.CyclicPartitioner.CyclicPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>CyclicPartitioner ()](#apidoc.element.kafka-node.CyclicPartitioner.CyclicPartitioner)
- description and source-code
```javascript
CyclicPartitioner = function () {
  this.c = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.CyclicPartitioner.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.CyclicPartitioner.</span>super_ ()](#apidoc.element.kafka-node.CyclicPartitioner.super_)
- description and source-code
```javascript
super_ = function () {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.CyclicPartitioner.prototype"></a>[module kafka-node.CyclicPartitioner.prototype](#apidoc.module.kafka-node.CyclicPartitioner.prototype)

#### <a name="apidoc.element.kafka-node.CyclicPartitioner.prototype.getPartition"></a>[function <span class="apidocSignatureSpan">kafka-node.CyclicPartitioner.prototype.</span>getPartition (partitions)](#apidoc.element.kafka-node.CyclicPartitioner.prototype.getPartition)
- description and source-code
```javascript
getPartition = function (partitions) {
  if (_.isEmpty(partitions)) return 0;
  return partitions[ this.c++ % partitions.length ];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.DefaultPartitioner"></a>[module kafka-node.DefaultPartitioner](#apidoc.module.kafka-node.DefaultPartitioner)

#### <a name="apidoc.element.kafka-node.DefaultPartitioner.DefaultPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>DefaultPartitioner ()](#apidoc.element.kafka-node.DefaultPartitioner.DefaultPartitioner)
- description and source-code
```javascript
DefaultPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.DefaultPartitioner.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.DefaultPartitioner.</span>super_ ()](#apidoc.element.kafka-node.DefaultPartitioner.super_)
- description and source-code
```javascript
super_ = function () {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.DefaultPartitioner.prototype"></a>[module kafka-node.DefaultPartitioner.prototype](#apidoc.module.kafka-node.DefaultPartitioner.prototype)

#### <a name="apidoc.element.kafka-node.DefaultPartitioner.prototype.getPartition"></a>[function <span class="apidocSignatureSpan">kafka-node.DefaultPartitioner.prototype.</span>getPartition (partitions)](#apidoc.element.kafka-node.DefaultPartitioner.prototype.getPartition)
- description and source-code
```javascript
getPartition = function (partitions) {
  if (partitions && _.isArray(partitions) && partitions.length > 0) {
    return partitions[0];
  } else {
    return 0;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.HighLevelConsumer"></a>[module kafka-node.HighLevelConsumer](#apidoc.module.kafka-node.HighLevelConsumer)

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.HighLevelConsumer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelConsumer (client, topics, options)](#apidoc.element.kafka-node.HighLevelConsumer.HighLevelConsumer)
- description and source-code
```javascript
HighLevelConsumer = function (client, topics, options) {
  if (!topics) {
    throw new Error('Must have payloads');
  }
  this.fetchCount = 0;
  this.client = client;
  this.options = _.defaults((options || {}), DEFAULTS);
  this.initialised = false;
  this.ready = false;
  this.closing = false;
  this.paused = this.options.paused;
  this.rebalancing = false;
  this.pendingRebalances = 0;
  this.committing = false;
  this.needToCommit = false;
  this.id = this.options.id || this.options.groupId + '_' + uuid.v4();
  this.payloads = this.buildPayloads(topics);
  this.topicPayloads = this.buildTopicPayloads(topics);
  this.connect();

  if (this.options.groupId) {
    validateConfig('options.groupId', this.options.groupId);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.</span>super_ ()](#apidoc.element.kafka-node.HighLevelConsumer.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.HighLevelConsumer.prototype"></a>[module kafka-node.HighLevelConsumer.prototype](#apidoc.module.kafka-node.HighLevelConsumer.prototype)

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype._releasePartitions"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>_releasePartitions (topicPayloads, callback)](#apidoc.element.kafka-node.HighLevelConsumer.prototype._releasePartitions)
- description and source-code
```javascript
_releasePartitions = function (topicPayloads, callback) {
  var self = this;
  async.each(topicPayloads, function (tp, cbb) {
    if (tp.partition !== undefined) {
      async.series([
        function (delcbb) {
          self.client.zk.checkPartitionOwnership(self.id, self.options.groupId, tp.topic, tp.partition, function (err) {
            if (err) {
              // Partition doesn't exist simply carry on
              cbb();
            } else delcbb();
          });
        },
        function (delcbb) {
          self.client.zk.deletePartitionOwnership(self.options.groupId, tp.topic, tp.partition, delcbb);
        },
        function (delcbb) {
          self.client.zk.checkPartitionOwnership(self.id, self.options.groupId, tp.topic, tp.partition, function (err) {
            if (err) {
              delcbb();
            } else {
              delcbb('Partition should not exist');
            }
          });
        }],
      cbb);
    } else {
      cbb();
    }
  }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.addTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>addTopics (topics, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.addTopics)
- description and source-code
```javascript
addTopics = function (topics, cb) {
  var self = this;
  if (!this.ready) {
    setTimeout(function () {
      self.addTopics(topics, cb);
    }, 100);
    return;
  }
  this.client.addTopics(
    topics,
    function (err, added) {
      if (err) return cb && cb(err, added);

      var payloads = self.buildPayloads(topics);
      // update offset of topics that will be added
      self.fetchOffset(payloads, function (err, offsets) {
        if (err) return cb(err);
        payloads.forEach(function (p) {
          var offset = offsets[p.topic][p.partition];
          if (offset === -1) offset = 0;
          p.offset = offset;
          self.topicPayloads.push(p);
        });
        // TODO: rebalance consumer
        cb && cb(null, added);
      });
    }
  );
}
```
- example usage
```shell
...
* 'topics': **Array**, array of topics to add
* 'cb': **Function**,the callback
* 'fromOffset': **Boolean**, if true, the consumer will fetch message from the specified offset, otherwise it will fetch message
 from the last commited offset of the topic.

Example:

''' js
consumer.addTopics(['t1', 't2'], function (err, added) {
});

or

consumer.addTopics([{ topic: 't1', offset: 10 }], function (err, added) {
}, true);
'''
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.autoCommit"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>autoCommit (force, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.autoCommit)
- description and source-code
```javascript
function autoCommit(force, cb) {
  if (arguments.length === 1) {
    cb = force;
    force = false;
  }

  if (!force) {
    if (this.committing) return cb(null, 'Offset committing');
    if (!this.needToCommit) return cb(null, 'Commit not needed');
  }

  this.needToCommit = false;
  this.committing = true;
  setTimeout(function () {
    this.committing = false;
  }.bind(this), this.options.autoCommitIntervalMs);

  var commits = this.topicPayloads.filter(function (p) { return p.offset !== -1; });

  if (commits.length) {
    this.sendOffsetCommitRequest(commits, cb);
  } else {
    cb(null, 'Nothing to be committed');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.buildPayloads"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>buildPayloads (payloads)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.buildPayloads)
- description and source-code
```javascript
buildPayloads = function (payloads) {
  var self = this;
  return payloads.map(function (p) {
    if (typeof p !== 'object') p = { topic: p };
    p.partition = p.partition || 0;
    p.offset = p.offset || 0;
    p.maxBytes = self.options.fetchMaxBytes;
    p.metadata = 'm'; // metadata can be arbitrary
    return p;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.buildTopicPayloads"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>buildTopicPayloads (topics)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.buildTopicPayloads)
- description and source-code
```javascript
buildTopicPayloads = function (topics) {
  return topics.map(function (j) {
    var k = { topic: j.topic };
    return k;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.close"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>close (force, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.close)
- description and source-code
```javascript
close = function (force, cb) {
  var self = this;
  this.ready = false;
  this.closing = true;
  clearInterval(this.checkPartitionOwnershipInterval);

  if (typeof force === 'function') {
    cb = force;
    force = false;
  }

  async.series([
    function (callback) {
      self.leaveGroup(callback);
    },
    function (callback) {
      if (force) {
        async.series([
          function (callback) {
            self.commit(true, callback);
          },
          function (callback) {
            self.client.close(callback);
          }
        ], callback);
        return;
      }
      self.client.close(callback);
    }
  ], cb);
}
```
- example usage
```shell
...

### close(force, cb)
* 'force': **Boolean**, if set to true, it forces the consumer to commit the current offset before closing, default 'false'

Example

'''js
consumer.close(true, cb);
consumer.close(cb); //force is disabled
'''

## HighLevelConsumer
⚠️ ***This consumer has been deprecated in the latest version of Kafka (0.10.1) and is likely to be removed in the future. Please
 use the ConsumerGroup instead.***

### HighLevelConsumer(client, payloads, options)
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.commit"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>commit (force, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.commit)
- description and source-code
```javascript
function autoCommit(force, cb) {
  if (arguments.length === 1) {
    cb = force;
    force = false;
  }

  if (!force) {
    if (this.committing) return cb(null, 'Offset committing');
    if (!this.needToCommit) return cb(null, 'Commit not needed');
  }

  this.needToCommit = false;
  this.committing = true;
  setTimeout(function () {
    this.committing = false;
  }.bind(this), this.options.autoCommitIntervalMs);

  var commits = this.topicPayloads.filter(function (p) { return p.offset !== -1; });

  if (commits.length) {
    this.sendOffsetCommitRequest(commits, cb);
  } else {
    cb(null, 'Nothing to be committed');
  }
}
```
- example usage
```shell
...
Commit offset of the current topics manually, this method should be called when a consumer leaves

* 'cb': **Function**, the callback

Example:

''' js
consumer.commit(function(err, data) {
});
'''

### setOffset(topic, partition, offset)
Set offset of the given topic

* 'topic': **String**
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.connect"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>connect ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.connect)
- description and source-code
```javascript
connect = function () {
  var self = this;
  // Client alreadyexists
  if (this.client.ready) {
    this.init();
  }

  this.client.on('ready', function () {
    if (!self.initialised) self.init();

    // Check the topics exist and create a watcher on them
    var topics = self.payloads.map(function (p) {
      return p.topic;
    });

    self.client.topicExists(topics, function (err) {
      if (err) {
        return self.emit('error', err);
      }
      self.initialised = true;
    });
  });

  function checkPartitionOwnership (callback) {
    async.each(self.topicPayloads, function (tp, cbb) {
      if (tp.partition !== undefined) {
        self.client.zk.checkPartitionOwnership(self.id, self.options.groupId, tp.topic, tp.partition, function (err) {
          if (err) {
            cbb(err);
          } else {
            cbb();
          }
        });
      } else {
        cbb();
      }
    }, callback);
  }

  // Check partition ownership and registration
  this.checkPartitionOwnershipInterval = setInterval(function () {
    if (!self.rebalancing) {
      async.parallel([
        checkPartitionOwnership,
        function (callback) {
          self.client.zk.isConsumerRegistered(self.options.groupId, self.id, function (error, registered) {
            if (error) {
              return callback(error);
            }
            if (registered) {
              callback();
            } else {
              callback(new Error(util.format('Consumer %s is not registered in group %s', self.id, self.options.groupId)));
            }
          });
        }
      ], function (error) {
        if (error) {
          self.emit('error', new errors.FailedToRegisterConsumerError(error.toString(), error));
        }
      });
    }
  }, 20000);

  function fetchAndUpdateOffsets (cb) {
    self.fetchOffset(self.topicPayloads, function (err, topics) {
      if (err) {
        return cb(err);
      }

      self.ready = true;
      self.updateOffsets(topics, true);

      return cb();
    });
  }

  function rebalance () {
    logger.debug('rebalance() %s is rebalancing: %s ready: %s', self.id, self.rebalancing, self.ready);
    if (!self.rebalancing && !self.closing) {
      deregister();

      self.emit('rebalancing');

      self.rebalancing = true;
      logger.debug('HighLevelConsumer rebalance retry config: %s', JSON.stringify(self.options.rebalanceRetry));
      var oldTopicPayloads = self.topicPayloads;
      var operation = retry.operation(self.options.rebalanceRetry);

      operation.attempt(function (currentAttempt) {
        self.rebalanceAttempt(oldTopicPayloads, function (err) {
          if (operation.retry(err)) {
            return;
          }
          if (err) {
            self.rebalancing = false;
            return self.emit('error', new errors.FailedToRebalanceConsumerError(operation.mainError().toString()));
          } else {
            var topicNames = self.topicPayloads.map(function (p) {
              return p.topic;
            });
            self.client.refreshMetadata(topicNames, function (err) {
              register();
              if (err) {
                self.rebalancing = false;
                self.emit('error', err);
                return;
              }

              if (self.topicPayloads.length) {
                fetchAndUpdateOffsets(function (err) {
                  self.rebalancing = false;
                  if (err) {
                    self.emit('error', new errors.FailedToRebalanceConsumerError(err.message));
                    return;
                  }
                  self.fetch();
                  self.emit('rebalanced');
                });
              } else { // was not assigned any partitions during rebalance
                self.rebalancing = false;
                self.emit('rebalanced');
              }
            });
          }
        });
      });
    }
  }

  // Wait for the consumer to be ready
  this.on('registered', rebalance);

  function register (fn) {
    logger.debug('Registered listeners %s', self.id);
    self.client.zk.on('consumersChanged', fn ...
```
- example usage
```shell
...
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}

util.inherits(ConsumerGroupMigrator, EventEmitter);
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.fetch"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>fetch ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.fetch)
- description and source-code
```javascript
fetch = function () {
  if (!this.ready || this.rebalancing || this.paused) {
    return;
  }

  this.client.sendFetchRequest(this, this.topicPayloads, this.options.fetchMaxWaitMs, this.options.fetchMinBytes, this.options.maxTickMessages
);
}
```
- example usage
```shell
...

Example

'''js
var kafka = require('kafka-node'),
    client = new kafka.Client(),
    offset = new kafka.Offset(client);
    offset.fetch([
        { topic: 't', partition: 0, time: Date.now(), maxNum: 1 }
    ], function (err, data) {
        // data
        // { 't': { '0': [999] } }
    });
'''
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.fetchOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>fetchOffset (payloads, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.fetchOffset)
- description and source-code
```javascript
fetchOffset = function (payloads, cb) {
  logger.debug('in fetchOffset %s payloads: %j', this.id, payloads);
  this.client.sendOffsetFetchRequest(this.options.groupId, payloads, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.getTopicPayloads"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>getTopicPayloads ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.getTopicPayloads)
- description and source-code
```javascript
getTopicPayloads = function () {
  if (!this.rebalancing) return this.topicPayloads;
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.init"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>init ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.init)
- description and source-code
```javascript
init = function () {
  var self = this;

  if (!self.topicPayloads.length) {
    return;
  }

  self.registerConsumer(function (err) {
    if (err) {
      return self.emit('error', new errors.FailedToRegisterConsumerError(err.toString()));
    }

    // Close the
    return self.emit('registered');
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.leaveGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>leaveGroup (cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.leaveGroup)
- description and source-code
```javascript
leaveGroup = function (cb) {
  var self = this;
  async.parallel([
    function (callback) {
      if (self.topicPayloads.length) {
        self._releasePartitions(self.topicPayloads, callback);
      } else {
        callback(null);
      }
    },
    function (callback) {
      self.client.zk.unregisterConsumer(self.options.groupId, self.id, callback);
    }
  ], cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.offsetRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>offsetRequest (payloads, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.offsetRequest)
- description and source-code
```javascript
offsetRequest = function (payloads, cb) {
  this.client.sendOffsetRequest(payloads, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.pause"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>pause ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.pause)
- description and source-code
```javascript
pause = function () {
  this.paused = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.rebalanceAttempt"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>rebalanceAttempt (oldTopicPayloads, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.rebalanceAttempt)
- description and source-code
```javascript
rebalanceAttempt = function (oldTopicPayloads, cb) {
  var self = this;
  // Do the rebalance.....
  var consumerPerTopicMap;
  var newTopicPayloads = [];
  logger.debug('HighLevelConsumer %s is attempting to rebalance', self.id);
  async.series([

    // Stop fetching data and commit offsets
    function (callback) {
      logger.debug('HighLevelConsumer %s stopping data read during rebalance', self.id);
      self.stop(function () {
        callback();
      });
    },

    // Assemble the data
    function (callback) {
      logger.debug('HighLevelConsumer %s assembling data for rebalance', self.id);
      self.client.zk.getConsumersPerTopic(self.options.groupId, function (err, obj) {
        if (err) {
          callback(err);
        } else {
          consumerPerTopicMap = obj;
          callback();
        }
      });
    },

    // Release current partitions
    function (callback) {
      logger.debug('HighLevelConsumer %s releasing current partitions during rebalance', self.id);
      self._releasePartitions(oldTopicPayloads, callback);
    },

    // Rebalance
    function (callback) {
      logger.debug('HighLevelConsumer %s determining the partitions to own during rebalance', self.id);
      logger.debug('consumerPerTopicMap.consumerTopicMap %j', consumerPerTopicMap.consumerTopicMap);
      for (var topic in consumerPerTopicMap.consumerTopicMap[self.id]) {
        if (!consumerPerTopicMap.consumerTopicMap[self.id].hasOwnProperty(topic)) {
          continue;
        }
        var topicToAdd = consumerPerTopicMap.consumerTopicMap[self.id][topic];
        var numberOfConsumers = consumerPerTopicMap.topicConsumerMap[topicToAdd].length;
        var numberOfPartition = consumerPerTopicMap.topicPartitionMap[topicToAdd].length;
        var partitionsPerConsumer = Math.floor(numberOfPartition / numberOfConsumers);
        var extraPartitions = numberOfPartition % numberOfConsumers;
        var currentConsumerIndex;
        for (var index in consumerPerTopicMap.topicConsumerMap[topicToAdd]) {
          if (!consumerPerTopicMap.topicConsumerMap[topicToAdd].hasOwnProperty(index)) {
            continue;
          }
          if (consumerPerTopicMap.topicConsumerMap[topicToAdd][index] === self.id) {
            currentConsumerIndex = parseInt(index);
            break;
          }
        }
        var extraBit = currentConsumerIndex;
        if (currentConsumerIndex > extraPartitions) extraBit = extraPartitions;
        var startPart = partitionsPerConsumer * currentConsumerIndex + extraBit;
        var extraNParts = 1;
        if (currentConsumerIndex + 1 > extraPartitions) extraNParts = 0;
        var nParts = partitionsPerConsumer + extraNParts;

        for (var i = startPart; i < startPart + nParts; i++) {
          newTopicPayloads.push({
            topic: topicToAdd,
            partition: consumerPerTopicMap.topicPartitionMap[topicToAdd][i],
            offset: 0,
            maxBytes: self.options.fetchMaxBytes,
            metadata: 'm'
          });
        }
      }
      logger.debug('newTopicPayloads %j', newTopicPayloads);
      callback();
    },

    // Update ZK with new ownership
    function (callback) {
      if (newTopicPayloads.length) {
        logger.debug('HighLevelConsumer %s gaining ownership of partitions during rebalance', self.id);
        async.eachSeries(newTopicPayloads, function (tp, cbb) {
          if (tp.partition !== undefined) {
            async.series([
              function (addcbb) {
                self.client.zk.checkPartitionOwnership(self.id, self.options.groupId, tp.topic, tp.partition, function (err) {
                  if (err) {
                    // Partition doesn't exist simply carry on
                    addcbb();
                  } else cbb(); // Partition exists simply carry on
                });
              },
              function (addcbb) {
                self.client.zk.addPartitionOwnership(self.id, self.options.groupId, tp.topic, tp.partition, function (err) {
                  if (err) {
                    addcbb(err);
                  } else addcbb(); ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.registerConsumer"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>registerConsumer (cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.registerConsumer)
- description and source-code
```javascript
registerConsumer = function (cb) {
  var self = this;
  var groupId = this.options.groupId;
  this.client.zk.registerConsumer(groupId, this.id, this.payloads, function (err) {
    if (err) return cb(err);
    self.client.zk.listConsumers(self.options.groupId);
    var topics = self.topicPayloads.reduce(function (ret, topicPayload) {
      if (ret.indexOf(topicPayload.topic) === -1) {
        ret.push(topicPayload.topic);
      }
      return ret;
    }, []);
    topics.forEach(function (topic) {
      self.client.zk.listPartitions(topic);
    });
    cb();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.removeTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>removeTopics (topics, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.removeTopics)
- description and source-code
```javascript
removeTopics = function (topics, cb) {
  topics = typeof topics === 'string' ? [topics] : topics;
  this.payloads = this.payloads.filter(function (p) {
    return !~topics.indexOf(p.topic);
  });

  this.client.removeTopicMetadata(topics, cb);
}
```
- example usage
```shell
...
### removeTopics(topics, cb)
* 'topics': **Array**, array of topics to remove
* 'cb': **Function**, the callback

Example:

''' js
consumer.removeTopics(['t1', 't2'], function (err, removed) {
});
'''

### commit(cb)
Commit offset of the current topics manually, this method should be called when a consumer leaves

* 'cb': **Function**, the callback
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.resume"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>resume ()](#apidoc.element.kafka-node.HighLevelConsumer.prototype.resume)
- description and source-code
```javascript
resume = function () {
  this.paused = false;
  this.fetch();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.sendOffsetCommitRequest"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>sendOffsetCommitRequest (commits, cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.sendOffsetCommitRequest)
- description and source-code
```javascript
sendOffsetCommitRequest = function (commits, cb) {
  this.client.sendOffsetCommitRequest(this.options.groupId, commits, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.setOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>setOffset (topic, partition, offset)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.setOffset)
- description and source-code
```javascript
setOffset = function (topic, partition, offset) {
  this.topicPayloads.every(function (p) {
    if (p.topic === topic && p.partition == partition) { // eslint-disable-line eqeqeq
      p.offset = offset;
      return false;
    }
    return true;
  });
}
```
- example usage
```shell
...
* 'partition': **Number**

* 'offset': **Number**

Example:

''' js
consumer.setOffset('topic', 0, 0);
'''

### pause()
Pause the consumer. ***Calling 'pause' does not automatically stop messages from being emitted.*** This is because pause just stops
 the kafka consumer fetch loop. Each iteration of the fetch loop can obtain a batch of messages (limited by 'fetchMaxBytes').

### resume()
Resume the consumer. Resumes the fetch loop.
...
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.stop"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>stop (cb)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.stop)
- description and source-code
```javascript
stop = function (cb) {
  if (!this.options.autoCommit) return cb && cb();
  this.commit(true, function (err) {
    cb && cb(err);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelConsumer.prototype.updateOffsets"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelConsumer.prototype.</span>updateOffsets (topics, initing)](#apidoc.element.kafka-node.HighLevelConsumer.prototype.updateOffsets)
- description and source-code
```javascript
updateOffsets = function (topics, initing) {
  this.topicPayloads.forEach(p => {
    if (!_.isEmpty(topics[p.topic]) && topics[p.topic][p.partition] !== undefined) {
      var offset = topics[p.topic][p.partition];
      if (offset === -1) offset = 0;
      if (!initing) p.offset = offset + 1;
      else p.offset = offset;
      this.needToCommit = true;
    }
  });

  if (this.options.autoCommit && !initing) {
    this.autoCommit(false, function (err) {
      err && logger.debug('auto commit offset', err);
    });
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.HighLevelProducer"></a>[module kafka-node.HighLevelProducer](#apidoc.module.kafka-node.HighLevelProducer)

#### <a name="apidoc.element.kafka-node.HighLevelProducer.HighLevelProducer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>HighLevelProducer (client, options, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer.HighLevelProducer)
- description and source-code
```javascript
function HighLevelProducer(client, options, customPartitioner) {
  BaseProducer.call(this, client, options, BaseProducer.PARTITIONER_TYPES.cyclic, customPartitioner);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.</span>super_ (client, options, defaultPartitionerType, customPartitioner)](#apidoc.element.kafka-node.HighLevelProducer.super_)
- description and source-code
```javascript
function BaseProducer(client, options, defaultPartitionerType, customPartitioner) {
  options = options || {};

  this.ready = false;
  this.client = client;

  this.requireAcks = options.requireAcks === undefined
    ? DEFAULTS.requireAcks
    : options.requireAcks;
  this.ackTimeoutMs = options.ackTimeoutMs === undefined
    ? DEFAULTS.ackTimeoutMs
    : options.ackTimeoutMs;

  if (customPartitioner !== undefined && options.partitionerType !== PARTITIONER_TYPES.custom) {
    throw new Error('Partitioner Type must be custom if providing a customPartitioner.');
  } else if (customPartitioner === undefined && options.partitionerType === PARTITIONER_TYPES.custom) {
    throw new Error('No customer partitioner defined');
  }

  var partitionerType = PARTITIONER_MAP[options.partitionerType] || PARTITIONER_MAP[defaultPartitionerType];

  // eslint-disable-next-line
  this.partitioner = new partitionerType(customPartitioner);

  this.connect();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.HighLevelProducer.super_"></a>[module kafka-node.HighLevelProducer.super_](#apidoc.module.kafka-node.HighLevelProducer.super_)

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.</span>super_ ()](#apidoc.element.kafka-node.HighLevelProducer.super_.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.HighLevelProducer.super_.prototype"></a>[module kafka-node.HighLevelProducer.super_.prototype](#apidoc.module.kafka-node.HighLevelProducer.super_.prototype)

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_.prototype.buildPayloads"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>buildPayloads (payloads, topicMetadata)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.buildPayloads)
- description and source-code
```javascript
buildPayloads = function (payloads, topicMetadata) {
  const topicPartitionRequests = Object.create(null);
  payloads.forEach((p) => {
    p.partition = p.hasOwnProperty('partition') ? p.partition : this.partitioner.getPartition(_.map(topicMetadata[p.topic], 'partition
'), p.key);
    p.attributes = p.hasOwnProperty('attributes') ? p.attributes : 0;
    let messages = _.isArray(p.messages) ? p.messages : [p.messages];

    messages = messages.map(function (message) {
      if (message instanceof KeyedMessage) {
        return message;
      }
      return new Message(0, 0, '', message);
    });

    let key = p.topic + p.partition;
    let request = topicPartitionRequests[key];

    if (request == null) {
      topicPartitionRequests[key] = new ProduceRequest(p.topic, p.partition, messages, p.attributes);
    } else {
      assert(request.attributes === p.attributes);
      Array.prototype.push.apply(request.messages, messages);
    }
  });
  return _.values(topicPartitionRequests);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_.prototype.close"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>close (cb)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  this.client.close(cb);
}
```
- example usage
```shell
...

### close(force, cb)
* 'force': **Boolean**, if set to true, it forces the consumer to commit the current offset before closing, default 'false'

Example

'''js
consumer.close(true, cb);
consumer.close(cb); //force is disabled
'''

## HighLevelConsumer
⚠️ ***This consumer has been deprecated in the latest version of Kafka (0.10.1) and is likely to be removed in the future. Please
 use the ConsumerGroup instead.***

### HighLevelConsumer(client, payloads, options)
...
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_.prototype.connect"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>connect ()](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.connect)
- description and source-code
```javascript
connect = function () {
  // emiter...
  var self = this;
  this.ready = this.client.ready;
  if (this.ready) self.emit('ready');
  this.client.on('ready', function () {
    if (!self.ready) {
      self.ready = true;
      self.emit('ready');
    }
  });
  this.client.on('brokersChanged', function () {
    let topics = Object.keys(this.topicMetadata);
    this.refreshMetadata(topics, function (error) {
      if (error) {
        self.emit('error', error);
      }
    });
  });
  this.client.on('error', function (err) {
    self.emit('error', err);
  });
  this.client.on('close', function () {});
}
```
- example usage
```shell
...
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}

util.inherits(ConsumerGroupMigrator, EventEmitter);
...
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_.prototype.createTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>createTopics (topics, async, cb)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.createTopics)
- description and source-code
```javascript
createTopics = function (topics, async, cb) {
  if (!this.ready) {
    return cb(new Error('Producer not ready!'));
  }

  this.client.createTopics(topics, async, cb);
}
```
- example usage
```shell
...

''' js
var kafka = require('kafka-node'),
    Producer = kafka.Producer,
    client = new kafka.Client(),
    producer = new Producer(client);
// Create topics sync
producer.createTopics(['t','t1'], false, function (err, data) {
    console.log(data);
});
// Create topics async
producer.createTopics(['t'], true, function (err, data) {});
producer.createTopics(['t'], function (err, data) {});// Simply omit 2nd arg
'''
...
```

#### <a name="apidoc.element.kafka-node.HighLevelProducer.super_.prototype.send"></a>[function <span class="apidocSignatureSpan">kafka-node.HighLevelProducer.super_.prototype.</span>send (payloads, cb)](#apidoc.element.kafka-node.HighLevelProducer.super_.prototype.send)
- description and source-code
```javascript
send = function (payloads, cb) {
  var client = this.client;
  var requireAcks = this.requireAcks;
  var ackTimeoutMs = this.ackTimeoutMs;

  client.sendProduceRequest(this.buildPayloads(payloads, client.topicMetadata), requireAcks, ackTimeoutMs, cb);
}
```
- example usage
```shell
...
    producer = new Producer(client),
    km = new KeyedMessage('key', 'message'),
    payloads = [
        { topic: 'topic1', messages: 'hi', partition: 0 },
        { topic: 'topic2', messages: ['hello', 'world', km] }
    ];
producer.on('ready', function () {
    producer.send(payloads, function (err, data) {
        console.log(data);
    });
});

producer.on('error', function (err) {})
'''
> ⚠️**WARNING**: Batch multiple messages of the same topic/partition together as an array on the 'messages' attribute otherwise
you may lose messages!
...
```



# <a name="apidoc.module.kafka-node.KeyedPartitioner"></a>[module kafka-node.KeyedPartitioner](#apidoc.module.kafka-node.KeyedPartitioner)

#### <a name="apidoc.element.kafka-node.KeyedPartitioner.KeyedPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>KeyedPartitioner ()](#apidoc.element.kafka-node.KeyedPartitioner.KeyedPartitioner)
- description and source-code
```javascript
KeyedPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.KeyedPartitioner.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.KeyedPartitioner.</span>super_ ()](#apidoc.element.kafka-node.KeyedPartitioner.super_)
- description and source-code
```javascript
super_ = function () {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.KeyedPartitioner.prototype"></a>[module kafka-node.KeyedPartitioner.prototype](#apidoc.module.kafka-node.KeyedPartitioner.prototype)

#### <a name="apidoc.element.kafka-node.KeyedPartitioner.prototype.getPartition"></a>[function <span class="apidocSignatureSpan">kafka-node.KeyedPartitioner.prototype.</span>getPartition (partitions, key)](#apidoc.element.kafka-node.KeyedPartitioner.prototype.getPartition)
- description and source-code
```javascript
getPartition = function (partitions, key) {
  key = key || '';

  var index = this.hashCode(key) % partitions.length;
  return partitions[index];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.KeyedPartitioner.prototype.hashCode"></a>[function <span class="apidocSignatureSpan">kafka-node.KeyedPartitioner.prototype.</span>hashCode (string)](#apidoc.element.kafka-node.KeyedPartitioner.prototype.hashCode)
- description and source-code
```javascript
hashCode = function (string) {
  var hash = 0;
  var length = string.length;

  for (var i = 0; i < length; i++) {
    hash = ((hash * 31) + string.charCodeAt(i)) & 0x7fffffff;
  }

  return (hash === 0) ? 1 : hash;
}
```
- example usage
```shell
...

  return (hash === 0) ? 1 : hash;
};

KeyedPartitioner.prototype.getPartition = function (partitions, key) {
  key = key || '';

  var index = this.hashCode(key) % partitions.length;
  return partitions[index];
};

var CustomPartitioner = function (partitioner) {
  this.getPartition = partitioner;
};
util.inherits(CustomPartitioner, Partitioner);
...
```



# <a name="apidoc.module.kafka-node.Offset"></a>[module kafka-node.Offset](#apidoc.module.kafka-node.Offset)

#### <a name="apidoc.element.kafka-node.Offset.Offset"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Offset (client)](#apidoc.element.kafka-node.Offset.Offset)
- description and source-code
```javascript
Offset = function (client) {
  var self = this;
  this.client = client;
  this.ready = this.client.ready;
  this.client.on('ready', function () {
    self.ready = true;
    self.emit('ready');
  });
  this.client.once('connect', function () {
    self.emit('connect');
  });
  this.client.on('error', function (err) {
    self.emit('error', err);
  });
}
```
- example usage
```shell
...
* 'cb': *Function*, the callback

Example

'''js
var kafka = require('kafka-node'),
    client = new kafka.Client(),
    offset = new kafka.Offset(client);
    offset.fetch([
        { topic: 't', partition: 0, time: Date.now(), maxNum: 1 }
    ], function (err, data) {
        // data
        // { 't': { '0': [999] } }
    });
'''
...
```

#### <a name="apidoc.element.kafka-node.Offset.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.</span>super_ ()](#apidoc.element.kafka-node.Offset.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.Offset.prototype"></a>[module kafka-node.Offset.prototype](#apidoc.module.kafka-node.Offset.prototype)

#### <a name="apidoc.element.kafka-node.Offset.prototype.buildPayloads"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>buildPayloads (payloads)](#apidoc.element.kafka-node.Offset.prototype.buildPayloads)
- description and source-code
```javascript
buildPayloads = function (payloads) {
  return payloads.map(function (p) {
    p.partition = p.partition || 0;
    p.time = p.time || Date.now();
    p.maxNum = p.maxNum || 1;
    p.metadata = 'm'; // metadata can be arbitrary
    return p;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Offset.prototype.commit"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>commit (groupId, payloads, cb)](#apidoc.element.kafka-node.Offset.prototype.commit)
- description and source-code
```javascript
commit = function (groupId, payloads, cb) {
  if (!this.ready) {
    this.once('ready', () => this.commit(groupId, payloads, cb));
    return;
  }
  this.client.sendOffsetCommitRequest(groupId, this.buildPayloads(payloads), cb);
}
```
- example usage
```shell
...
Commit offset of the current topics manually, this method should be called when a consumer leaves

* 'cb': **Function**, the callback

Example:

''' js
consumer.commit(function(err, data) {
});
'''

### setOffset(topic, partition, offset)
Set offset of the given topic

* 'topic': **String**
...
```

#### <a name="apidoc.element.kafka-node.Offset.prototype.fetch"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetch (payloads, cb)](#apidoc.element.kafka-node.Offset.prototype.fetch)
- description and source-code
```javascript
fetch = function (payloads, cb) {
  if (!this.ready) {
    this.once('ready', () => this.fetch(payloads, cb));
    return;
  }
  this.client.sendOffsetRequest(this.buildPayloads(payloads), cb);
}
```
- example usage
```shell
...

Example

'''js
var kafka = require('kafka-node'),
    client = new kafka.Client(),
    offset = new kafka.Offset(client);
    offset.fetch([
        { topic: 't', partition: 0, time: Date.now(), maxNum: 1 }
    ], function (err, data) {
        // data
        // { 't': { '0': [999] } }
    });
'''
...
```

#### <a name="apidoc.element.kafka-node.Offset.prototype.fetchCommits"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetchCommits (groupId, payloads, cb)](#apidoc.element.kafka-node.Offset.prototype.fetchCommits)
- description and source-code
```javascript
fetchCommits = function (groupId, payloads, cb) {
  if (!this.ready) {
    this.once('ready', () => this.fetchCommits(groupId, payloads, cb));
    return;
  }
  this.client.sendOffsetFetchRequest(groupId, this.buildPayloads(payloads), cb);
}
```
- example usage
```shell
...

Example

'''js
var kafka = require('kafka-node'),
    client = new kafka.Client(),
    offset = new kafka.Offset(client);
    offset.fetchCommits('groupId', [
        { topic: 't', partition: 0 }
    ], function (err, data) {
    });
'''

### fetchLatestOffsets(topics, cb)
...
```

#### <a name="apidoc.element.kafka-node.Offset.prototype.fetchEarliestOffsets"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetchEarliestOffsets (topics, cb)](#apidoc.element.kafka-node.Offset.prototype.fetchEarliestOffsets)
- description and source-code
```javascript
fetchEarliestOffsets = function (topics, cb) {
  fetchOffsets(this, topics, cb, -2);
}
```
- example usage
```shell
...
### fetchEarliestOffsets(topics, cb)

Example

'''js
	var partition = 0;
	var topic = 't';
	offset.fetchEarliestOffsets([topic], function (error, offsets) {
		if (error)
			return handleError(error);
		console.log(offsets[topic][partition]);
	});
'''

# Troubleshooting / FAQ
...
```

#### <a name="apidoc.element.kafka-node.Offset.prototype.fetchLatestOffsets"></a>[function <span class="apidocSignatureSpan">kafka-node.Offset.prototype.</span>fetchLatestOffsets (topics, cb)](#apidoc.element.kafka-node.Offset.prototype.fetchLatestOffsets)
- description and source-code
```javascript
fetchLatestOffsets = function (topics, cb) {
  fetchOffsets(this, topics, cb, -1);
}
```
- example usage
```shell
...
### fetchLatestOffsets(topics, cb)

Example

'''js
	var partition = 0;
	var topic = 't';
	offset.fetchLatestOffsets([topic], function (error, offsets) {
		if (error)
			return handleError(error);
		console.log(offsets[topic][partition]);
	});
'''

### fetchEarliestOffsets(topics, cb)
...
```



# <a name="apidoc.module.kafka-node.Producer"></a>[module kafka-node.Producer](#apidoc.module.kafka-node.Producer)

#### <a name="apidoc.element.kafka-node.Producer.Producer"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>Producer (client, options, customPartitioner)](#apidoc.element.kafka-node.Producer.Producer)
- description and source-code
```javascript
function Producer(client, options, customPartitioner) {
  BaseProducer.call(this, client, options, BaseProducer.PARTITIONER_TYPES.default, customPartitioner);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.Producer.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.Producer.</span>super_ (client, options, defaultPartitionerType, customPartitioner)](#apidoc.element.kafka-node.Producer.super_)
- description and source-code
```javascript
function BaseProducer(client, options, defaultPartitionerType, customPartitioner) {
  options = options || {};

  this.ready = false;
  this.client = client;

  this.requireAcks = options.requireAcks === undefined
    ? DEFAULTS.requireAcks
    : options.requireAcks;
  this.ackTimeoutMs = options.ackTimeoutMs === undefined
    ? DEFAULTS.ackTimeoutMs
    : options.ackTimeoutMs;

  if (customPartitioner !== undefined && options.partitionerType !== PARTITIONER_TYPES.custom) {
    throw new Error('Partitioner Type must be custom if providing a customPartitioner.');
  } else if (customPartitioner === undefined && options.partitionerType === PARTITIONER_TYPES.custom) {
    throw new Error('No customer partitioner defined');
  }

  var partitionerType = PARTITIONER_MAP[options.partitionerType] || PARTITIONER_MAP[defaultPartitionerType];

  // eslint-disable-next-line
  this.partitioner = new partitionerType(customPartitioner);

  this.connect();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.RandomPartitioner"></a>[module kafka-node.RandomPartitioner](#apidoc.module.kafka-node.RandomPartitioner)

#### <a name="apidoc.element.kafka-node.RandomPartitioner.RandomPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>RandomPartitioner ()](#apidoc.element.kafka-node.RandomPartitioner.RandomPartitioner)
- description and source-code
```javascript
RandomPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.RandomPartitioner.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.RandomPartitioner.</span>super_ ()](#apidoc.element.kafka-node.RandomPartitioner.super_)
- description and source-code
```javascript
super_ = function () {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.RandomPartitioner.prototype"></a>[module kafka-node.RandomPartitioner.prototype](#apidoc.module.kafka-node.RandomPartitioner.prototype)

#### <a name="apidoc.element.kafka-node.RandomPartitioner.prototype.getPartition"></a>[function <span class="apidocSignatureSpan">kafka-node.RandomPartitioner.prototype.</span>getPartition (partitions)](#apidoc.element.kafka-node.RandomPartitioner.prototype.getPartition)
- description and source-code
```javascript
getPartition = function (partitions) {
  return partitions[Math.floor(Math.random() * partitions.length)];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.consumerGroupMigrator"></a>[module kafka-node.consumerGroupMigrator](#apidoc.module.kafka-node.consumerGroupMigrator)

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.consumerGroupMigrator"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupMigrator (consumerGroup)](#apidoc.element.kafka-node.consumerGroupMigrator.consumerGroupMigrator)
- description and source-code
```javascript
function ConsumerGroupMigrator(consumerGroup) {
  EventEmitter.call(this);
  assert(consumerGroup);
  const self = this;
  this.consumerGroup = consumerGroup;
  this.client = consumerGroup.client;
  var verified = 0;

  if (consumerGroup.options.migrateRolling) {
    this.zk = zookeeper.createClient(consumerGroup.client.connectionString, {retries: 10});
    this.zk.on('connected', function () {
      self.filterByExistingZkTopics(function (error, topics) {
        if (error) {
          return self.emit('error', error);
        }

        if (topics.length) {
          self.checkForOwnersAndListenForChange(topics);
        } else {
          logger.debug('No HLC topics exist in zookeeper.');
          self.connectConsumerGroup();
        }
      });
    });

    this.on('noOwnersForTopics', function (topics) {
      logger.debug('No owners for topics %s reported.', topics);
      if (++verified <= NUMER_OF_TIMES_TO_VERIFY) {
        logger.debug('%s verify %d of %d HLC has given up ownership by checking again in %d', self.client.clientId, verified,
          NUMER_OF_TIMES_TO_VERIFY, VERIFY_WAIT_TIME_MS);

        setTimeout(function () {
          self.checkForOwners(topics);
        }, VERIFY_WAIT_TIME_MS);
      } else {
        self.connectConsumerGroup();
      }
    });

    this.on('topicOwnerChange', _.debounce(function (topics) {
      verified = 0;
      self.checkForOwnersAndListenForChange(topics);
    }, 250));

    this.zk.connect();
  } else {
    this.connectConsumerGroup();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.super_"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.</span>super_ ()](#apidoc.element.kafka-node.consumerGroupMigrator.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.consumerGroupMigrator.prototype"></a>[module kafka-node.consumerGroupMigrator.prototype](#apidoc.module.kafka-node.consumerGroupMigrator.prototype)

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.prototype.checkForOwners"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>checkForOwners (topics, listenForChange)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.checkForOwners)
- description and source-code
```javascript
checkForOwners = function (topics, listenForChange) {
  const self = this;
  const path = '/consumers/' + this.consumerGroup.options.groupId + '/owners/';
  var ownedPartitions = 0;

  function topicWatcher (event) {
    self.emit('topicOwnerChange', topics);
  }

  async.each(topics,
    function (topic, callback) {
      const args = [path + topic];

      if (listenForChange) {
        logger.debug('%s listening for changes in topic %s', self.client.clientId, topic);
        args.push(topicWatcher);
      }

      args.push(function (error, children, stats) {
        if (error) {
          return callback(error);
        }
        ownedPartitions += children.length;
        callback(null);
      });

      self.zk.getChildren.apply(self.zk, args);
    },
    function (error) {
      if (error) {
        return self.emit('error', error);
      }
      if (ownedPartitions === 0) {
        self.emit('noOwnersForTopics', topics);
      } else {
        logger.debug('%s %d partitions are owned by old HLC... waiting...', self.client.clientId, ownedPartitions);
      }
    }
  );
}
```
- example usage
```shell
...
this.on('noOwnersForTopics', function (topics) {
  logger.debug('No owners for topics %s reported.', topics);
  if (++verified <= NUMER_OF_TIMES_TO_VERIFY) {
    logger.debug('%s verify %d of %d HLC has given up ownership by checking again in %d', self.client.clientId, verified,
      NUMER_OF_TIMES_TO_VERIFY, VERIFY_WAIT_TIME_MS);

    setTimeout(function () {
      self.checkForOwners(topics);
    }, VERIFY_WAIT_TIME_MS);
  } else {
    self.connectConsumerGroup();
  }
});

this.on('topicOwnerChange', _.debounce(function (topics) {
...
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.prototype.checkForOwnersAndListenForChange"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>checkForOwnersAndListenForChange (topics)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.checkForOwnersAndListenForChange)
- description and source-code
```javascript
checkForOwnersAndListenForChange = function (topics) {
  this.checkForOwners(topics, true);
}
```
- example usage
```shell
...
this.zk.on('connected', function () {
  self.filterByExistingZkTopics(function (error, topics) {
    if (error) {
      return self.emit('error', error);
    }

    if (topics.length) {
      self.checkForOwnersAndListenForChange(topics);
    } else {
      logger.debug('No HLC topics exist in zookeeper.');
      self.connectConsumerGroup();
    }
  });
});
...
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.prototype.connectConsumerGroup"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>connectConsumerGroup ()](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.connectConsumerGroup)
- description and source-code
```javascript
connectConsumerGroup = function () {
  logger.debug('%s connecting consumer group', this.client.clientId);
  const self = this;
  if (this.client.ready) {
    this.consumerGroup.connect();
  } else {
    this.client.once('ready', function () {
      self.consumerGroup.connect();
    });
  }
  this.zk && this.zk.close();
}
```
- example usage
```shell
...
      return self.emit('error', error);
    }

    if (topics.length) {
      self.checkForOwnersAndListenForChange(topics);
    } else {
      logger.debug('No HLC topics exist in zookeeper.');
      self.connectConsumerGroup();
    }
  });
});

this.on('noOwnersForTopics', function (topics) {
  logger.debug('No owners for topics %s reported.', topics);
  if (++verified <= NUMER_OF_TIMES_TO_VERIFY) {
...
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.prototype.filterByExistingZkTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>filterByExistingZkTopics (callback)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.filterByExistingZkTopics)
- description and source-code
```javascript
filterByExistingZkTopics = function (callback) {
  const self = this;
  const path = '/consumers/' + this.consumerGroup.options.groupId + '/owners/';

  async.filter(this.consumerGroup.topics, function (topic, cb) {
    const topicPath = path + topic;
    logger.debug('%s checking zk path %s', self.client.clientId, topicPath);
    self.zk.exists(topicPath, function (error, stat) {
      if (error) {
        return callback(error);
      }
      cb(stat);
    });
  }, function (result) {
    callback(null, result);
  });
}
```
- example usage
```shell
...
  this.consumerGroup = consumerGroup;
  this.client = consumerGroup.client;
  var verified = 0;

  if (consumerGroup.options.migrateRolling) {
    this.zk = zookeeper.createClient(consumerGroup.client.connectionString, {retries: 10});
    this.zk.on('connected', function () {
      self.filterByExistingZkTopics(function (error, topics) {
if (error) {
  return self.emit('error', error);
}

if (topics.length) {
  self.checkForOwnersAndListenForChange(topics);
} else {
...
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.prototype.getOffset"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>getOffset (tp, defaultOffset)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.getOffset)
- description and source-code
```javascript
getOffset = function (tp, defaultOffset) {
  const offset = _.get(this.offsets, [tp.topic, tp.partition], defaultOffset);
  if (offset === -1) {
    return defaultOffset;
  }
  return offset;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.consumerGroupMigrator.prototype.saveHighLevelConsumerOffsets"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupMigrator.prototype.</span>saveHighLevelConsumerOffsets (topicPartitionList, callback)](#apidoc.element.kafka-node.consumerGroupMigrator.prototype.saveHighLevelConsumerOffsets)
- description and source-code
```javascript
saveHighLevelConsumerOffsets = function (topicPartitionList, callback) {
  const self = this;
  this.client.sendOffsetFetchRequest(this.consumerGroup.options.groupId, topicPartitionList, function (error, results) {
    logger.debug('sendOffsetFetchRequest response:', results, error);
    if (error) {
      return callback(error);
    }
    self.offsets = results;
    callback(null);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.consumerGroupRecovery"></a>[module kafka-node.consumerGroupRecovery](#apidoc.module.kafka-node.consumerGroupRecovery)

#### <a name="apidoc.element.kafka-node.consumerGroupRecovery.consumerGroupRecovery"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>consumerGroupRecovery (consumerGroup)](#apidoc.element.kafka-node.consumerGroupRecovery.consumerGroupRecovery)
- description and source-code
```javascript
function ConsumerGroupRecovery(consumerGroup) {
  this.consumerGroup = consumerGroup;
  this.options = consumerGroup.options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.consumerGroupRecovery.prototype"></a>[module kafka-node.consumerGroupRecovery.prototype](#apidoc.module.kafka-node.consumerGroupRecovery.prototype)

#### <a name="apidoc.element.kafka-node.consumerGroupRecovery.prototype.clearError"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupRecovery.prototype.</span>clearError ()](#apidoc.element.kafka-node.consumerGroupRecovery.prototype.clearError)
- description and source-code
```javascript
clearError = function () {
  this.lastError = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.consumerGroupRecovery.prototype.getRetryTimeout"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupRecovery.prototype.</span>getRetryTimeout (error)](#apidoc.element.kafka-node.consumerGroupRecovery.prototype.getRetryTimeout)
- description and source-code
```javascript
getRetryTimeout = function (error) {
  assert(error);
  if (!this._timeouts) {
    this._timeouts = retry.timeouts({
      retries: this.options.retries,
      factor: this.options.retryFactor,
      minTimeout: this.options.retryMinTimeout
    });
  }

  if (this._retryIndex == null || this.lastError == null ||
      error.errorCode !== this.lastError.errorCode) {
    this._retryIndex = 0;
  }

  var index = this._retryIndex++;
  if (index >= this._timeouts.length) {
    return false;
  }
  return this._timeouts[index];
}
```
- example usage
```shell
...
    recoverableItem.handler && recoverableItem.handler.call(this.consumerGroup, error);
    return true;
  }
  return false;
}, this);

if (retry) {
  retryTimeout = this.getRetryTimeout(error);
}

if (retry && retryTimeout) {
  logger.debug('RECOVERY from %s: %s retrying in %s ms', source, this.consumerGroup.client.clientId, retryTimeout, error);
  this.consumerGroup.scheduleReconnect(retryTimeout);
} else {
  this.consumerGroup.emit('error', error);
...
```

#### <a name="apidoc.element.kafka-node.consumerGroupRecovery.prototype.tryToRecoverFrom"></a>[function <span class="apidocSignatureSpan">kafka-node.consumerGroupRecovery.prototype.</span>tryToRecoverFrom (error, source)](#apidoc.element.kafka-node.consumerGroupRecovery.prototype.tryToRecoverFrom)
- description and source-code
```javascript
tryToRecoverFrom = function (error, source) {
  this.consumerGroup.ready = false;
  this.consumerGroup.stopHeartbeats();

  var retryTimeout = false;
  var retry = recoverableErrors.some(function (recoverableItem) {
    if (isErrorInstanceOf(error, recoverableItem.errors)) {
      recoverableItem.handler && recoverableItem.handler.call(this.consumerGroup, error);
      return true;
    }
    return false;
  }, this);

  if (retry) {
    retryTimeout = this.getRetryTimeout(error);
  }

  if (retry && retryTimeout) {
    logger.debug('RECOVERY from %s: %s retrying in %s ms', source, this.consumerGroup.client.clientId, retryTimeout, error);
    this.consumerGroup.scheduleReconnect(retryTimeout);
  } else {
    this.consumerGroup.emit('error', error);
  }
  this.lastError = error;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.logging"></a>[module kafka-node.logging](#apidoc.module.kafka-node.logging)

#### <a name="apidoc.element.kafka-node.logging.logging"></a>[function <span class="apidocSignatureSpan">kafka-node.</span>logging (name)](#apidoc.element.kafka-node.logging.logging)
- description and source-code
```javascript
function getLogger(name) {
  return loggerProvider(name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.logging.setLoggerProvider"></a>[function <span class="apidocSignatureSpan">kafka-node.logging.</span>setLoggerProvider (provider)](#apidoc.element.kafka-node.logging.setLoggerProvider)
- description and source-code
```javascript
function setLoggerProvider(provider) {
  loggerProvider = provider;
}
```
- example usage
```shell
...
### How do I set a logger provider?

For performance reasons, initialization of the 'kafka-node' module creates all necessary loggers. This means that custom logger
providers need to be set *before requiring the 'kafka-node' module*. The following example shows how this can be done:

'''javascript
// first configure the logger provider
const kafkaLogging = require('kafka-node/logging');
kafkaLogging.setLoggerProvider(consoleLoggerProvider);

// then require kafka-node and continue as normal
const kafka = require('kafka-node');
'''

# Running Tests
...
```



# <a name="apidoc.module.kafka-node.partitioner"></a>[module kafka-node.partitioner](#apidoc.module.kafka-node.partitioner)

#### <a name="apidoc.element.kafka-node.partitioner.CustomPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>CustomPartitioner (partitioner)](#apidoc.element.kafka-node.partitioner.CustomPartitioner)
- description and source-code
```javascript
CustomPartitioner = function (partitioner) {
  this.getPartition = partitioner;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.partitioner.CyclicPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>CyclicPartitioner ()](#apidoc.element.kafka-node.partitioner.CyclicPartitioner)
- description and source-code
```javascript
CyclicPartitioner = function () {
  this.c = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.partitioner.DefaultPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>DefaultPartitioner ()](#apidoc.element.kafka-node.partitioner.DefaultPartitioner)
- description and source-code
```javascript
DefaultPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.partitioner.KeyedPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>KeyedPartitioner ()](#apidoc.element.kafka-node.partitioner.KeyedPartitioner)
- description and source-code
```javascript
KeyedPartitioner = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.partitioner.RandomPartitioner"></a>[function <span class="apidocSignatureSpan">kafka-node.partitioner.</span>RandomPartitioner ()](#apidoc.element.kafka-node.partitioner.RandomPartitioner)
- description and source-code
```javascript
RandomPartitioner = function () {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.utils"></a>[module kafka-node.utils](#apidoc.module.kafka-node.utils)

#### <a name="apidoc.element.kafka-node.utils.createTopicPartitionList"></a>[function <span class="apidocSignatureSpan">kafka-node.utils.</span>createTopicPartitionList (topicPartitions)](#apidoc.element.kafka-node.utils.createTopicPartitionList)
- description and source-code
```javascript
function createTopicPartitionList(topicPartitions) {
  var tpList = [];
  for (var topic in topicPartitions) {
    if (!topicPartitions.hasOwnProperty(topic)) {
      continue;
    }
    topicPartitions[topic].forEach(function (partition) {
      tpList.push({
        topic: topic,
        partition: partition
      });
    });
  }
  return tpList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.utils.groupPartitionsByTopic"></a>[function <span class="apidocSignatureSpan">kafka-node.utils.</span>groupPartitionsByTopic (topicPartitions)](#apidoc.element.kafka-node.utils.groupPartitionsByTopic)
- description and source-code
```javascript
function groupPartitionsByTopic(topicPartitions) {
  assert(Array.isArray(topicPartitions));
  return topicPartitions.reduce(function (result, tp) {
    if (!(tp.topic in result)) {
      result[tp.topic] = [tp.partition];
    } else {
      result[tp.topic].push(tp.partition);
    }
    return result;
  }, {});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.utils.validateConfig"></a>[function <span class="apidocSignatureSpan">kafka-node.utils.</span>validateConfig (property, value)](#apidoc.element.kafka-node.utils.validateConfig)
- description and source-code
```javascript
function validateConfig(property, value) {
  if (!legalChars.test(value)) {
    throw new InvalidConfigError([property, value, "is illegal, contains a character other than ASCII alphanumerics, '.', '_' and
 '-'"].join(' '));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.utils.validateTopicNames"></a>[function <span class="apidocSignatureSpan">kafka-node.utils.</span>validateTopicNames (topics)](#apidoc.element.kafka-node.utils.validateTopicNames)
- description and source-code
```javascript
function validateTopicNames(topics) {
  // Rewriting same validations done by Apache Kafka team for topics
  // iterating over topics
  topics.some(function (topic) {
    if (topic.length <= 0) {
      throw new InvalidConfigError('topic name is illegal, cannot be empty');
    }
    if (topic === '.' || topic === '..') {
      throw new InvalidConfigError('topic name cannot be . or ..');
    }
    if (topic.length > allowedTopicLength) {
      throw new InvalidConfigError('topic name is illegal, cannot be longer than ${allowedTopicLength} characters');
    }
    if (!legalChars.test(topic)) {
      throw new InvalidConfigError('topic name ${topic} is illegal, contains a character other than ASCII alphanumerics .,_ and -');
    }
  });
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.utils.validateTopics"></a>[function <span class="apidocSignatureSpan">kafka-node.utils.</span>validateTopics (topics)](#apidoc.element.kafka-node.utils.validateTopics)
- description and source-code
```javascript
function validateTopics(topics) {
  if (topics.some(function (topic) {
    if ('partition' in topic) {
      return typeof topic.partition !== 'number';
    }
    return false;
  })) {
    throw new InvalidConfigError('Offset must be a number and can not contain characters');
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kafka-node.zookeeper"></a>[module kafka-node.zookeeper](#apidoc.module.kafka-node.zookeeper)

#### <a name="apidoc.element.kafka-node.zookeeper.Zookeeper"></a>[function <span class="apidocSignatureSpan">kafka-node.zookeeper.</span>Zookeeper (connectionString, options)](#apidoc.element.kafka-node.zookeeper.Zookeeper)
- description and source-code
```javascript
Zookeeper = function (connectionString, options) {
  this.client = zookeeper.createClient(connectionString, options);

  var that = this;
  this.client.on('connected', function () {
    that.listBrokers();
  });
  this.client.on('disconnected', function () {
    that.emit('disconnected');
  });
  this.client.connect();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kafka-node.zookeeper.ZookeeperConsumerMappings"></a>[function <span class="apidocSignatureSpan">kafka-node.zookeeper.</span>ZookeeperConsumerMappings ()](#apidoc.element.kafka-node.zookeeper.ZookeeperConsumerMappings)
- description and source-code
```javascript
ZookeeperConsumerMappings = function () {
  this.consumerTopicMap = {};
  this.topicConsumerMap = {};
  this.topicPartitionMap = {};
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
