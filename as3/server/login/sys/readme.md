`sys` XML Packet Data Type
==========================

__Data Type__              : `sys`

__Data Type abbreviation : `system`__

## General Structure

```xml
<msg t='sys'>
    <body action = "ACTION*" [ t = '' ] r = '-1'> 
      [ <k><![CDATA[DATA]]></k> ]
      [ <vars> <var [n=''] t=''><![CDATA[DATA]]></var> ... </vars> ]
	</body>
</msg>
```

`...*` denotes the item is mandatory

`[...]` denotes the item is optional
