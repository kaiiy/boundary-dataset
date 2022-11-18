# 市町村境界線データ

「国土数値情報（行政区域データ）」（国土交通省）（https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-N03-v3_0.html#prefecture00）を加工して作成

## unpack

```sh
$ cat packets/pk-* > boundary.json.bz2
$ bzip2 -d boundary.json.bz2
```

## pack

```sh
$ bzip2 boundary.json
$ split -b 5M boundary.json.bz2 packets/pk-
```

