scan_signal.sh
==================

UHF チャンネルのスキャンをする。

使い方
-------

端末で:

```sh
$ ./scan_signal.sh        # UHF チャンネルすべてをスキャンする
$ ./scan_signal.sh 16     # UHF 16 だけスキャンする
$ ./scan_signal.sh 16 22  # UHF 16 と 22 をスキャンする
```

`PATH` にない、`recpt1` とか `epgdump` を使うときは:

```sh
$ RECPT1=/path/to/recpt1 EPGDUMP=/path/to/epgdump ./scan_signal.sh
```

用意するもの
-----------

* recpt1
* epgdump (無くても動く、あるとチャンネル名を表示する)

注意
----

C/N が時々 nandb になってしまう。その時は、`./scan_signal.sh <チャンネル>` で
特定のチャンネルだけ再度スキャンし直す。
