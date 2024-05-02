## "Compilation" to a stand-alone binary

This is as easy as running the following command:

```
deno compile --allow-read --allow-write ./gen.ts
```

# my sticky notes:

## 1:

the as_path filters used:

is the asn in the path?
`bgp_path ~ [= * <ASN> * =]`

is the carrier + the asn in the path?
`bgp_path ~ [= * <CARRIER> <ASN> * =]`

## 2:

get just the aspa dump from routinator:

```
routinator --enable-aspa vrps -f json -o /root/dump.json --no-route-origins --no-router-keys
```

this is probably missing a flag to skip tls verification for idiots (the ASAs are signed anyway?):

`[WARN] RRDP https://rpki.cnnic.cn/rrdp/notify.xml: error sending request for url (https://rpki.cnnic.cn/rrdp/notify.xml): error trying to connect: invalid peer certificate: UnknownIssuer`