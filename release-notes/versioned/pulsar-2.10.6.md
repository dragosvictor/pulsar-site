---
id: pulsar-2.10.6
title: Apache Pulsar 2.10.6
sidebar_label: Apache Pulsar 2.10.6
---

#### 2024-3-8
## Broker

### Improvements

- [improve][broker] Consistently add fine-grain authorization to REST API [22202](https://github.com/apache/pulsar/pull/22202)
- [improve] [broker] Do not print an Error log when responding to `HTTP-404` when calling `Admin API` and the topic does not exist. [21995](https://github.com/apache/pulsar/pull/21995)
- [improve][proxy] Fix comment about enableProxyStatsEndpoints [21757](https://github.com/apache/pulsar/pull/21757)
- [improve][broker][PIP-318] Support not retaining null-key message during topic compaction [21578](https://github.com/apache/pulsar/pull/21578)
- [improve] [client] Merge lookup requests for the same topic [21232](https://github.com/apache/pulsar/pull/21232)
- [improve] [broker] Let the producer request success at the first time if the previous one is inactive [21220](https://github.com/apache/pulsar/pull/21220)
- [improve] [proxy] Not close the socket if lookup failed caused by too many requests [21216](https://github.com/apache/pulsar/pull/21216)
- [improve] [broker] Not close the socket if lookup failed caused by bundle unloading or metadata ex [21211](https://github.com/apache/pulsar/pull/21211)
- [improve] [broker] Print warn log if ssl handshake error & print ledger id when switch ledger [21201](https://github.com/apache/pulsar/pull/21201)
- [improve] [broker] improve read entry error log for troubleshooting [21169](https://github.com/apache/pulsar/pull/21169)
- [improve][proxy] Support disabling metrics endpoint [21031](https://github.com/apache/pulsar/pull/21031)
- [improve][broker] Improve cache handling for partitioned topic metadata when doing lookup [21063](https://github.com/apache/pulsar/pull/21063)
- [improve][broker] Avoid print redirect exception log when get list from bundle [20846](https://github.com/apache/pulsar/pull/20846)
- [improve][sql] Fix the wrong format of the logs [20907](https://github.com/apache/pulsar/pull/20907)
- [improve][broker] Add consumer-id into the log when doing subscribe. [20568](https://github.com/apache/pulsar/pull/20568)
- [improve] [broker] Print warn log if compaction failure [19405](https://github.com/apache/pulsar/pull/19405)
- [improve][admin]internalGetMessageById shouldn't be allowed on partitioned topic [19013](https://github.com/apache/pulsar/pull/19013)

### Fixes

- [fix][sec] Upgrade Jetty to 9.4.54.v20240208 to address CVE-2024-22201 [22144](https://github.com/apache/pulsar/pull/22144)
- [fix][sec] Upgrade commons-compress to 1.26.0 [22086](https://github.com/apache/pulsar/pull/22086)
- [fix][broker] Support running docker container with gid != 0 [22081](https://github.com/apache/pulsar/pull/22081)
- [fix][broker] Sanitize values before logging in apply-config-from-env.py script [22044](https://github.com/apache/pulsar/pull/22044)
- [fix][broker][branch-3.1] Avoid PublishRateLimiter use an already closed RateLimiter [22011](https://github.com/apache/pulsar/pull/22011)
- [fix] [broker] Replication stopped due to unload topic failed [21947](https://github.com/apache/pulsar/pull/21947)
- [fix] [broker] fix write all compacted out entry into compacted topic [21917](https://github.com/apache/pulsar/pull/21917)
- [fix] [ml] Fix retry mechanism of deleting ledgers to invalidate [21869](https://github.com/apache/pulsar/pull/21869)
- [fix][broker]Fix NonPersistentDispatcherMultipleConsumers ArrayIndexOutOfBoundsException [21856](https://github.com/apache/pulsar/pull/21856)
- [fix][broker] Fix String wrong format [21829](https://github.com/apache/pulsar/pull/21829)
- [fix] [broker] Update topic policies as much as possible when some ex was thrown [21810](https://github.com/apache/pulsar/pull/21810)
- [fix][broker] Fix the wrong value of BrokerSrevice.maxUnackedMsgsPerDispatcher [21765](https://github.com/apache/pulsar/pull/21765)
- [fix][sec] Exclude avro from hadoop-client [21719](https://github.com/apache/pulsar/pull/21719)
- [fix][test] Fix PerformanceProducer send count error [21706](https://github.com/apache/pulsar/pull/21706)
- [fix][broker] Fix the issue of topics possibly being deleted. [21704](https://github.com/apache/pulsar/pull/21704)
- [fix][broker] Fix typo in the config key [21690](https://github.com/apache/pulsar/pull/21690)
- [fix] [broker] network package lost if enable haProxyProtocolEnabled [21684](https://github.com/apache/pulsar/pull/21684)
- [fix][broker] Fix memory leak during topic compaction [21647](https://github.com/apache/pulsar/pull/21647)
- [fix][broker] Duplicate LedgerOffloader creation when namespace/topic… [21591](https://github.com/apache/pulsar/pull/21591)
- [fix][broker] Correct schema deletion for partitioned topic [21574](https://github.com/apache/pulsar/pull/21574)
- [fix][broker] Fix namespace bundle stuck in unloading status (#21445) [21567](https://github.com/apache/pulsar/pull/21567)
- [fix][broker] Fix create topic with different auto creation strategies causes race condition [21545](https://github.com/apache/pulsar/pull/21545)
- [fix] [ml] Fix orphan scheduled task for ledger create timeout check [21542](https://github.com/apache/pulsar/pull/21542)
- [fix] [broker] Fix thousands orphan PersistentTopic caused OOM [21540](https://github.com/apache/pulsar/pull/21540)
- [fix][ml] Fix unfinished callback when deleting managed ledger [21530](https://github.com/apache/pulsar/pull/21530)
- [fix][broker] Fix setReplicatedSubscriptionStatus incorrect behavior [21510](https://github.com/apache/pulsar/pull/21510)
- [fix][broker] Do not write replicated snapshot marker when the topic which is not enable replication [21495](https://github.com/apache/pulsar/pull/21495)
- [branch-2.10][fix][proxy] Move status endpoint out of auth coverage [21494](https://github.com/apache/pulsar/pull/21494)
- [fix][broker] Avoid pass null role in MultiRolesTokenAuthorizationProvider [21486](https://github.com/apache/pulsar/pull/21486)
- [fix][broker] Fix the deadlock when using BookieRackAffinityMapping with rackaware policy [21481](https://github.com/apache/pulsar/pull/21481)
- [fix][broker] Fix namespace bundle stuck in unloading status [21445](https://github.com/apache/pulsar/pull/21445)
- [fix][broker] Fix MultiRoles token provider NPE when using anonymous clients [21429](https://github.com/apache/pulsar/pull/21429)
- [fix][proxy] Move status endpoint out of auth coverage [21428](https://github.com/apache/pulsar/pull/21428)
- [fix][sec] Upgrade Netty to 4.1.100 to address CVE-2023-44487 [21397](https://github.com/apache/pulsar/pull/21397)
- [fix][sec] Bump avro version to 1.11.3 for CVE-2023-39410 [21341](https://github.com/apache/pulsar/pull/21341)
- [fix][test] Fix flaky test NarUnpackerTest [21328](https://github.com/apache/pulsar/pull/21328)
- [fix] [bk-client]  Fix bk client MinNumRacksPerWriteQuorum and EnforceMinNumRacksPerWriteQuorum not work problem.  [21327](https://github.com/apache/pulsar/pull/21327)
- [fix][ml] Fix thread safe issue with RangeCache.put and RangeCache.clear [21302](https://github.com/apache/pulsar/pull/21302)
- [fix][sec] Upgrade snappy-java to 1.1.10.5 [21280](https://github.com/apache/pulsar/pull/21280)
- [fix][txn] Ack all message ids when ack chunk messages with transaction. [21268](https://github.com/apache/pulsar/pull/21268)
- [fix][broker][branch-2.10] Fix inconsistent topic policy [21258](https://github.com/apache/pulsar/pull/21258)
- [fix] [ml] fix wrong msg backlog of non-durable cursor after trim ledgers [21250](https://github.com/apache/pulsar/pull/21250)
- [fix] [ml] Reader can set read-pos to a deleted ledger [21248](https://github.com/apache/pulsar/pull/21248)
- [fix][broker]Fixed produce and consume when anonymousUserRole enabled [21237](https://github.com/apache/pulsar/pull/21237)
- [fix][broker] Fix inconsistent topic policy [21231](https://github.com/apache/pulsar/pull/21231)
- [fix][broker] Fixed reset for AggregatedNamespaceStats [21225](https://github.com/apache/pulsar/pull/21225)
- [fix][broker] Make the new exclusive consumer instead the inactive one faster [21183](https://github.com/apache/pulsar/pull/21183)
- [fix][broker][branch-2.10] Backport fix UniformLoadShedder selecet wrong overloadbroker and underloadbroker [21182](https://github.com/apache/pulsar/pull/21182)
- [Branch-2.10] [imporve] [bookie] Upgrade BookKeeper dependency to 4.14.8 for branch 2.10 [21148](https://github.com/apache/pulsar/pull/21148)
- [fix][client] Fix repeat consume when using n-ack and batched messages [21116](https://github.com/apache/pulsar/pull/21116)
- [fix][client] Avoid ack hole for chunk message [21101](https://github.com/apache/pulsar/pull/21101)
- [branch-2.10] [fix] [broker] Fix isolated group not work problem. [21098](https://github.com/apache/pulsar/pull/21098)
- [fix] [broker] Fix isolated group not work problem. [21096](https://github.com/apache/pulsar/pull/21096)
- [fix][broker] Fix write duplicate entries into the compacted ledger after RawReader reconnects [21081](https://github.com/apache/pulsar/pull/21081)
- [fix][client] Fix consumer can't consume resent chunked messages [21070](https://github.com/apache/pulsar/pull/21070)
- [fix][broker] Make sure all inflight writes have finished  before completion of compaction [21067](https://github.com/apache/pulsar/pull/21067)
- [fix][broker] Use MessageDigest.isEqual when comparing digests [21061](https://github.com/apache/pulsar/pull/21061)
- [fix][misc] Bump GRPC version to 1.55.3 to fix CVE [21057](https://github.com/apache/pulsar/pull/21057)
- [fix] [bk] Correctct the bookie info after ZK client is reconnected [21035](https://github.com/apache/pulsar/pull/21035)
- [fix][io] Update test certs for Elasticsearch [21001](https://github.com/apache/pulsar/pull/21001)
- [fix][broker] Fix can't stop phase-two of compaction even though messageId read reaches lastReadId [20988](https://github.com/apache/pulsar/pull/20988)
- [fix][broker] Fix message loss during topic compaction [20980](https://github.com/apache/pulsar/pull/20980)
- [fix][broker] Fix incorrect number of read compacted entries [20978](https://github.com/apache/pulsar/pull/20978)
- [fix][broker]Fix chunked messages will be filtered by duplicating [20948](https://github.com/apache/pulsar/pull/20948)
- [fix][broker]Check that the super user role is in the MultiRolesTokenAuthorizationProvider plugin [20939](https://github.com/apache/pulsar/pull/20939)
- [fix] [log] fix the vague response if topic not found [20932](https://github.com/apache/pulsar/pull/20932)
- [fix][broker] fix MessageDeduplication throw NPE when enable broker dedup and set namespace disable deduplication. [20905](https://github.com/apache/pulsar/pull/20905)
- [fix] [ml] fix discontinuous ledger deletion [20898](https://github.com/apache/pulsar/pull/20898)
- [fix][broker] In replication scenario, remote consumer could not be registered if there has no message was sent [20888](https://github.com/apache/pulsar/pull/20888)
- [branch-2.10][fix][broker] Fix inconsensus namespace policies by getPoliciesIfCached [20873](https://github.com/apache/pulsar/pull/20873)
- [branch-2.10][fix][broker] Inconsistent behaviour for topic auto_creation [20872](https://github.com/apache/pulsar/pull/20872)
- [fix][broker] Fix inconsensus namespace policies by `getPoliciesIfCached` [20855](https://github.com/apache/pulsar/pull/20855)
- [fix][broker] Avoid infinite bundle unloading [20822](https://github.com/apache/pulsar/pull/20822)
- [fix][broker] Fix get topic policies as null during clean cache [20763](https://github.com/apache/pulsar/pull/20763)
- [fix] [broker] do not filter system topic while shedding. [18949](https://github.com/apache/pulsar/pull/18949)
- [improve] Introduce the sync() API to ensure consistency on reads during critical metadata operation paths [18518](https://github.com/apache/pulsar/pull/18518)
- [fix][broker] Fix namespace not found will cause request timeout [18512](https://github.com/apache/pulsar/pull/18512)
- [fix][io] exclude logback dependency for canal connector [18226](https://github.com/apache/pulsar/pull/18226)
