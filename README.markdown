# pHash-0.9.6-patches

pHash-0.9.6 was released at 2013-04-23, but there are 2 major problems for certain usage, so I patches:

1. Compatible with new PHP version (Compile/Install passed).
2. Change `ph_dct_imagehash()` function to return hash string for further operation.

## Installation

### Ubuntu

#### 1. pHash

```
$ sudo apt-get install libavformat-dev libmpg123-dev libsamplerate-dev libsndfile-dev
$ sudo apt-get install cimg-dev libavcodec-dev ffmpeg libswscale-dev
```

```
$ cd pHash-0.9.6a
$ ./configure
$ make && sudo make install
```

#### 2. PHP binding

```
$ cd bindings/php
$ phpize
$ ./configure LIBS="-lpthread"
$ make && sudo make install
```

```
$ sudo vi /etc/php5/conf.d/pHash.so
extension=pHash.so
```

```
$ sudo php5enmod pHash
```

```
$ php -m
pHash
```

## Reference

1. https://github.com/lucidix/phash/commit/5be2d454c932152e9b2395e21f97a008c6bd8766
2. https://github.com/eaccelerator/eaccelerator/issues/33
3. http://serverfault.com/questions/491730/compile-phash-on-centos-php-extension

## License

Same as [pHash](http://www.phash.org/), [GPL-3.0](http://www.gnu.org/licenses/gpl-3.0.html).
