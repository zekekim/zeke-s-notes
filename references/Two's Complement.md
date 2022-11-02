---
reference: Cornell CS
section: 
date: 2022-11-01
tags: #comp-arch
---

If the number in two's complement has a leading `1` it is a negative number, and if it has a leading `0` it is a positive number.

For example, for the decimal number `-12`, first write it in positive form as `12`.

`0000 1100`

Then, the negative number is written as flipped digits and an added `1`, which is known as its two's complement.

`1111 0100`

You can add this to positive `30`, let's write it out.

```
0001 1110 //  30
1111 0100 // -12
0001 0010 //  18
```

If something is stored in two's complement, just apply two's complement to it again.
