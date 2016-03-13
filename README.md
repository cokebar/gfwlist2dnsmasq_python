gfwlist2dnsmasq
=================
Intro
-----
Just another script to auto-generate dnsmasq ipset rules using gfwlist

__Notification: Need python2, do not use python3__

GFWList is composed by regular expressions, but dnsmasq rules is formed by domain names. So the conversion from GFWList to dnsmasq rule list is not a equivalent conversion. You might need to add extra rules or modify some converted rules.

Using:
-----

Modify gfwlist2dnsmasq.py:

Change this to your DNS server IP&port:
```python
mydnsip = '127.0.0.1'
mydnsport = '5353'
```

Change this to your ipset name:
```python
ipsetname = 'gfwlist'
```

Path to save you rule file:
```python
rulefile = './dnsmasq_list.conf'
```

Add your own extra domain here. One domain in a line. eg:
```python
EX_DOMAIN=[ \
'.google.com', \
'.google.com.hk', \
'.google.com.tw', \
'.google.com.sg', \
'.google.co.jp', \
'.blogspot.com', \
'.blogspot.sg', \
'.blogspot.hk', \
'.blogspot.jp', \
'.gvt1.com', \
'.gvt2.com', \
'.gvt3.com', \
'.1e100.net', \
'.blogspot.tw' \
]
```
Then run gfwlist2dnsmasq.py:
```bash
python gfwlist2dnsmasq.py
```
If you don't want to generate the rules by yourself, you can download the rule file from:

https://github.com/cokebar/gfwlist2dnsmasq/releases
