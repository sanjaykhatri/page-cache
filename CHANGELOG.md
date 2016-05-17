PageCache ChangeLog
===================

### 1.3.0 (Work in progress)

* PSR-2 coding style adopted (php-cs-fixer and phpcs are being used)
* File locking mechanism using flock(). Single write - many reads of the same cache file.
* Stampede protection (Dog pile effect) added.
* PSR-3 Logger integration (PageCache already comes with a simple logging support). 
* Storage support added. This will enable to store cache not only in files. Currently FileSystem only.
* More tests added. 
* PSR-0 support removed from php-cs-fixer (As of 2014-10-21 PSR-0 has been marked as deprecated. PSR-4 is now recommended as an alternative.)

### 1.2.3 (2016-05-10)

* PHPUnit tests added to tests/, along with needed phpunit.xml settings and testing bootstrap. You can run PHPUnit tests easily on entire library.
* PHPUnit tests developed with full coverage for all classes, except PageCache class.
* Composer autoload-dev now loads tests/
* SessionHandler uses serialize() now.
* MobileStrategy now accepts $mobileDetect parameter. Useful for testing, but not only.
* Travis support added. PageCache successfully passes on PHP 5.5, 5.6 on Travis.

### 1.2.2 (2016-05-23)

* More session support improvements. SessionHandler class added.
* session_exclude_keys config parameter added, along with sessionExclude() method.
* HashDirectory update.
* General improvements.

### 1.2.1 (2016-04-22)

* MobileStrategy bug fixed, session wasn't contained inside md5().

### 1.2.0 (2016-04-22)

* Session support added to PageCache.
* All Strategies were updated to support sessions.
* Composer installation instructions added

### 1.1.0 (2016-04-20)

* clearPageCache() introduced to clear current page cache.
* Added getPageCache() and getFile() methods to PageCache class.
* Default value for min_cache_file_size was reduced to 10 from 1000.
* Examples updates

### 1.0.1 (2016-04-19)

* Improvements.
* Examples, README updates.

### 1.0.0   (2016-04-17)

* Initial release.