# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [18845380](https://bscscan.com/block/18845380)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.18845380.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 534.68 gb, 546.26 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 7e31d15f52b4f0529b6048a1a336a2e82768c4fa168d5d6737a3dc08c75fd24e
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

!!! from block [18839890](https://bscscan.com/block/18839890)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.18839890.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 788.64 gb, 1803.00 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 45ce67cddbf445403dac00893915cbfe24c7120df71d3066a3ec9e66b306b0c6
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--snapshots=false --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000
```
