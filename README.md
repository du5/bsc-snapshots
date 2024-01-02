# *bsc-snapshots*


- *[Geth](#geth)*
    - *[Geth full node with pbss](#geth-full-node-with-pbss)*
    - *[Geth fast node](#geth-fast-node)*
    - *[Geth full node](#geth-full-node)*
- *[How to download](#how-to-download)*
    - *[pipeline download and extract](#pipeline-download-and-extract)*
    - *[multithreaded download](#multithreaded-download)*

## Geth
### Geth full node with pbss

| Field |Value |
| --- | --- |
| Version | [v1.3.7](https://github.com/bnb-chain/bsc/releases/tag/v1.3.7) |
| Block | [34712063](https://bscscan.com/block/34712063) (Dec-27-2023 05:55:40 AM +UTC) |
| Link | `https://snapshots.48.club/geth.pbss.34712063.tar.zst` |
| Size | 767.36G <-> 904.04G |
| SHA256 | `a6d9c259b309731522da1c221727d421a9c1fb3eaf6b9ba5a0c9d7aa3904d8b4` |
| Flags | `--history.transactions=0 --syncmode=full --tries-verify-mode=local --pruneancient --db.engine=pebble --state.scheme=path` |
| Disk Suggestion | Minimum(NVMe ≥ 1T), Suggestion(NVMe ≥ 2T)|

[Back to TOC](#bsc-snapshots)

### Geth fast node

| Field |Value |
| --- | --- |
| Version | [v1.3.7](https://github.com/bnb-chain/bsc/releases/tag/v1.3.7) |
| Block | [34744407](https://bscscan.com/block/34744407) (Dec-28-2023 08:55:31 AM +UTC) |
| Link | `https://snapshots.48.club/geth.fast.34744407.tar.zst` |
| Size | 362.00G <-> 413.77G |
| SHA256 | `0aef466ed2a3e01842f739857db43e120bb9b4474188f012755ba8e4a5f873bf` |
| Flags | `--history.transactions=0 --syncmode=full --tries-verify-mode=none --pruneancient --db.engine=pebble` |
| Disk Suggestion | Minimum(NVMe ≥ 500G), Suggestion(NVMe ≥ 1T)|

[Back to TOC](#bsc-snapshots)

### Geth full node

| Field |Value |
| --- | --- |
| Version | [v1.3.7](https://github.com/bnb-chain/bsc/releases/tag/v1.3.7) |
| Block | [34882141](https://bscscan.com/block/34882141) (Jan-02-2024 03:56:41 AM +UTC) |
| Link | `https://snapshots.48.club/geth.full.34882141.tar.zst` |
| Size | 983.84G <-> 1081.33G |
| SHA256 | `020e0151ff45170d5f767a86b5895af72f56f19d5e144b23e5a0b9a4b1e447c4` |
| Flags | `--history.transactions=0 --syncmode=full --tries-verify-mode=local --pruneancient --db.engine=pebble` |
| Disk Suggestion | Minimum(NVMe ≥ 2T), Suggestion(NVMe ≥ 3T)|

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
