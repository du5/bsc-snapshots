# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

**This geth snapshot is generated with `--tries-verify-mode=none` so it contains no MPT data. You should not build a validator upon this snapshot. [Know more >>>](https://github.com/bnb-chain/bsc/pull/926)**

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours
Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.16)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.16) for sync


### download

<!-- begin_geth -->

!!! from block [22125232](https://bscscan.com/block/22125232)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.bnb48.club/geth.22125232.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.22125232.tar.lz4 -o geth.tar.lz4
```


### checksum

!!! db size 306.52 gb, 312.38 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= d066d616ab28a46e0f3691571f0a6057e7057dc0bba99c39784942f7fc589bf5
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync=true --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2.28.1)](https://github.com/ledgerwatch/erigon/releases/tag/v2.28.1) for sync


### download

<!-- begin_erigon -->

!!! from block [22210056](https://bscscan.com/block/22210056)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.bnb48.club/erigon.22210056.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.22210056.tar.lz4 -o erigon.tar.lz4
```


### checksum

!!! db size 848.73 gb, 1242.99 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 95a6933ec166f4b2cadb6df48055afcb91f5f7711ecd395841cb7b03d387306d
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune=hrtc --db.pagesize=16k
```
