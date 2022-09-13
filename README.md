# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours

Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.13)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.13) for sync


### download

<!-- begin_geth -->

!!! from block [21303408](https://bscscan.com/block/21303408)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.21303408.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 576.59 gb, 589.06 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 5bd82257ac7f104199de8ea2e270339d8df6ba4f8624ad22ab15851d43b7864d
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync=true --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2022.09.01)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.09.01) for sync


### download

<!-- begin_erigon -->

!!! from block [21302085](https://bscscan.com/block/21302085)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.21302085.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 816.19 gb, 1189.60 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 3a3fe8eead19142fe1fc078354777d0ed986a806829d23d4a9b22d1f6c7b457c
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune=hrtc --db.pagesize=16k
```
