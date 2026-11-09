Team project specific README
# Internal dissection structure through tshark
```plain
[('dns.id_raw', ['f675', 28, 2, 0, 5]),
 ('dns.id', '0xf675'),
 ('dns.flags_raw', ['0100', 30, 2, 0, 5]),
 ('dns.flags', '0x0100'),
 ('dns.flags_tree',
  [('dns.flags.response_raw', ['0', 30, 2, 32768, 2]),
   ('dns.flags.response', '0'),
   ('dns.flags.opcode_raw', ['0', 30, 2, 30720, 5]),
   ('dns.flags.opcode', '0'),
   ('dns.flags.truncated_raw', ['0', 30, 2, 512, 2]),
   ('dns.flags.truncated', '0'),
   ('dns.flags.recdesired_raw', ['1', 30, 2, 256, 2]),
   ('dns.flags.recdesired', '1'),
   ('dns.flags.z_raw', ['0', 30, 2, 64, 2]),
   ('dns.flags.z', '0'),
   ('dns.flags.checkdisable_raw', ['0', 30, 2, 16, 2]),
   ('dns.flags.checkdisable', '0')]),
 ('dns.count.queries_raw', ['0001', 32, 2, 0, 5]),
 ('dns.count.queries', '1'),
 ('dns.count.answers_raw', ['0000', 34, 2, 0, 5]),
 ('dns.count.answers', '0'),
 ('dns.count.auth_rr_raw', ['0000', 36, 2, 0, 5]),
 ('dns.count.auth_rr', '0'),
 ('dns.count.add_rr_raw', ['0000', 38, 2, 0, 5]),
 ('dns.count.add_rr', '0'),
 ('Queries',
  [('a0.twimg.com: type A, class IN',
    [('dns.qry.name_raw', ['026130057477696d6703636f6d00', 40, 14, 0, 26]),
     ('dns.qry.name', 'a0.twimg.com'),
     ('dns.qry.name.len_raw', ['026130057477696d6703636f6d00', 40, 14, 0, 5]),
     ('dns.qry.name.len', '12'),
     ('dns.count.labels_raw', ['026130057477696d6703636f6d00', 40, 14, 0, 5]),
     ('dns.count.labels', '3'),
     ('dns.qry.type_raw', ['0001', 54, 2, 0, 5]),
     ('dns.qry.type', '1'),
     ('dns.qry.class_raw', ['0001', 56, 2, 0, 5]),
     ('dns.qry.class', '0x0001')])])]
```
- ['f675', 28, 2, 0, 5]
  - `f675` is the HEX value of the field
  - `28` is the offset from the packet to the protocol part
  - `2` is the length in bytes
  - `5` is the field type, see [here](https://github.com/wireshark/wireshark/blob/master/doc/README.display_filter)
