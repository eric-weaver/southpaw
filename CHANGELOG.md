# Change log

## 0.4.1
May 14th, 2019

### Bug Fixes
* Cap the size on the fronting set in the ByteArraySet class to prevent uncontrolled growth and OOM errors [#42](https://github.com/jwplayer/southpaw/pull/42) 

## 0.4.0
May 9th, 2019

### New Features
* Add optional setting for configuring RocksDB log level

### Bug Fixes
* Avoid excessive RocksDB column family flushes [#41](https://github.com/jwplayer/southpaw/pull/41) *Note: This change may lead to higher memory utilization than previously experienced as we are flushing memory to disk less often with the trade off of more efficient read/writes*

## 0.3.2
April 30th, 2019

### Bug Fixes
* Keep track of and close all iterators on RocksDBState close [#40](https://github.com/jwplayer/southpaw/pull/40)
* Catch and optionally ignore the proper s3 exceptions [#39](https://github.com/jwplayer/southpaw/pull/39)
* Shutdown threadpools when shutting down RocksDbState instances [#38](https://github.com/jwplayer/southpaw/pull/38)
* Move topic ordering outside the main loop [#34](https://github.com/jwplayer/southpaw/pull/34)
* Add logging around syncFromS3 [#33](https://github.com/jwplayer/southpaw/pull/33)
* Ensure RocksDB closes on exceptions [#32](https://github.com/jwplayer/southpaw/pull/32)

## 0.3.1
April 11th, 2019

### Bug Fixes
* Fix potential memory leak in KafkaTopics.flush() [#31](https://github.com/jwplayer/southpaw/pull/31)

## 0.3.0
April 3rd, 2019

### New Features
* Add support for restore modes [#30](https://github.com/jwplayer/southpaw/pull/30)
* Add optional setting for auto restoring previous rocksdb backup [#23](https://github.com/jwplayer/southpaw/pull/23)

### Bug Fixes
* Cleanup SouthpawTest temp directories [#29](https://github.com/jwplayer/southpaw/pull/29)
* Cleanup temporary directory usage [#28](https://github.com/jwplayer/southpaw/pull/28)
* Remove unused curator-framework dependency[#25](https://github.com/jwplayer/southpaw/pull/25)
* Cleanup tests that write to disk[#24](https://github.com/jwplayer/southpaw/pull/24)
* Cleanup rocksdb options reference handling [#22](https://github.com/jwplayer/southpaw/pull/22)
* Close backup engine when no backups [#21](https://github.com/jwplayer/southpaw/pull/21)

## 0.2.4
March 5th, 2019

* Ensure rocksdb backup engine closes [#20](https://github.com/jwplayer/southpaw/pull/20)

## 0.2.3
February 21st, 2019

* Fixes a thread leak in S3Helper [#19](https://github.com/jwplayer/southpaw/pull/19)

## 0.2.2
February 20th, 2019

* Reduced # of flushes with RocksDB state [#18](https://github.com/jwplayer/southpaw/pull/18)  

## 0.2.1
January 11th, 2019

[#16](https://github.com/jwplayer/southpaw/pull/16)
* Simplified filter functionality 
* Added new metrics for filters
* Made RocksDB S3 syncs for backups run in a background thread
* Added new metrics for S3 functionality
* Added new setting to allow errors in syncs to S3 to not kill Southpaw 

## 0.2.0
January 8th, 2018

* Add support for object change detection in filters [#2](https://github.com/jwplayer/southpaw/pull/2)
* Bump jackson versions [#13](https://github.com/jwplayer/southpaw/pull/13)
* Add travis ci [#12](https://github.com/jwplayer/southpaw/pull/12)
* Ensure rocksdb test directories are created/deleted [#11](https://github.com/jwplayer/southpaw/pull/11)

## 0.1.0

* Initial release
