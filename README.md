# *bsc-snapshots*


- *[Geth](#geth)*
    - *[Geth fast node](#geth-fast-node)*
    - *[Geth full node](#geth-full-node)*
- *[Erigon](#erigon)*
    - *[Erigon fast node](#erigon-fast-node)*
- *[How to download](#how-to-download)*
    - *[pipeline download and extract](#pipeline-download-and-extract)*
    - *[multithreaded download](#multithreaded-download)*

## Geth
### Geth fast node

| Field |Value |
| --- | --- |
| Version | [v1.4.14](https://github.com/bnb-chain/bsc/releases/tag/v1.4.14) |
| Block | [42091528](https://bscscan.com/block/42091528) (Sep-09-2024 03:08:45 AM +UTC) |
| Link | `https://snapshots.48.club/geth.fast.42091528.tar.zst` |
| Size | 318.25G <-> 350.54G |
| SHA256 | `9d2699eb3e3972f5d1cb51e976867cf1919cda46d496600dffd3f6494e65dd60` |
| Flags | `--history.transactions=90000 --syncmode=full --db.engine=pebble --tries-verify-mode=none` |
| Disk Suggestion | Minimum(NVMe ≥ 500G), Suggestion(NVMe ≥ 1T)|

[Back to TOC](#bsc-snapshots)

### Geth full node

| Field |Value |
| --- | --- |
| Version | [v1.4.14](https://github.com/bnb-chain/bsc/releases/tag/v1.4.14) |
| Block | [42093177](https://bscscan.com/block/42093177) (Sep-09-2024 04:31:34 AM +UTC) |
| Link | `https://snapshots.48.club/geth.full.42093177.tar.zst` |
| Size | 867.98G <-> 949.04G |
| SHA256 | `7bb562c3f360d4a937c53a7343e9b902f38ba80a5434834dd2213fe9d53da28d` |
| Flags | `--history.transactions=90000 --syncmode=full --db.engine=pebble` |
| Disk Suggestion | Minimum(NVMe ≥ 1.2T), Suggestion(NVMe ≥ 2T)|

[Back to TOC](#bsc-snapshots)

## Erigon
### Erigon fast node

| Field |Value |
| --- | --- |
| Version | [v1.2.15](https://github.com/node-real/bsc-erigon/releases/tag/v1.2.15) |
| Tips | Comimg sooooon! |

[Back to TOC](#bsc-snapshots)

## How to download
### pipeline download and extract

```bash
wget $Link -O - | zstd -cd | tar xf -
```

### multithreaded download

```bash
aria2c -s4 -x4 -k1024M $Link -o $save_path
zstd -cd $save_path | tar xf -
openssl sha256 $save_path # checksum verification, optional
```

[Back to TOC](#bsc-snapshots)
