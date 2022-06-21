# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [18875617](https://bscscan.com/block/18875617)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.18875617.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 542.30 gb, 553.94 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 97c7a8552f6050e5bcc649bf7745ba013f3970e4e9cee3b0a2fb0c32e27b21d2
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync --syncmode=snap
```


## erigon-snapshots


> Database uses [erigon(v2022.06.01)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.06.01) for sync


### download

<!-- begin_erigon -->

!!! from block [18879302](https://bscscan.com/block/18879302)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.18879302.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 787.22 gb, 1803.00 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 1684db28b0d0edd7faa1224bf3dc4ac8ce8c5059f9fc55a6e1f6f3d1ba4ffcb8
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--snapshots=false --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000
```
