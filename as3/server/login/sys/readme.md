`sys` XML Packet Data Type
==========================

__Data Type__              : `sys`

__Data Type abbreviation : `system`__

## General Structure

```
<msg t='sys'>
    <body action = "ACTION*" [ t = '' ] r = '-1'> 
      [ <k><![CDATA[DATA]]></k> ]
	</body>
</msg>
```

`...*` denotes the item is mandatory

`[...]` denotes the item is optional
