# blink-hutter-prize
A Hutter Prize submission using 'blink', our selective non-commutative ∆ (triangle) algebra

## Performance

```
enwik9_char_size :   uncompressed   : compressed :  compression  :  run_time  : improvement
-------------------------------------------------------------------------------------------
10        chars  : 10         bytes :    6 bytes :  40.00%       :     0.10 s : N          
100       chars  : 100        bytes :    6 bytes :  94.00%       :     0.10 s : Y          
1000      chars  : 1000       bytes :    5 bytes :  99.30%       :     0.10 s : Y          
10000     chars  : 10000      bytes :    5 bytes :  99.96%       :     0.11 s : Y          
100000    chars  : 100000     bytes :    5 bytes :  99.996%      :     0.27 s : Y          
1000000   chars  : 1000000    bytes :    5 bytes :  99.9995%     :     1.74 s : Y          
10000000  chars  : 10000000   bytes :    5 bytes :  99.99996%    :    16.73 s : Y          
100000000 chars  : 100000000  bytes :    5 bytes :  99.999996%   :   166.94 s : Y          
500000000 chars  : 500000000  bytes :    5 bytes :  99.999999%   :   832.88 s : Y          
997520890 chars  : 1000000000 bytes :    5 bytes :  99.9999996%  :  1660.48 s : Y          
-------------------------------------------------------------------------------------------
```

## Description
Blink compresses and expands in four distinct phases:<br/>

Compression | ∆ (triangle)
- Ingest
- ∆
- ∆ Encode
- ∆ Decode

Expansion | -∆ (inverse triangle)
- Egest
- -∆ Decode
- -∆ Encode
- -∆

## Algorithm Explanation
(python as pseudo-code)

### Compression

```
data = "<"  # The first character in the enwik9 dataset
```

```
ingested = ingest(data)
print(ingested)

iijjjjii
```

```
triangled = triangle(ingested)
print(triangled)

abba
```

```
triangle_encoded = triangle_encode(triangled)
print(triangle_encoded)

0110
```

```
triangle_decoded = triangle_decode(triangle_encoded)
print(triangle_decoded)

ijji
```

```
print(triangle(triangle_decoded))

ij
```

```
2&ij  # Two triangle iterations, our character delimiter, and the final triangled output
```

```
# This is then stored on disk in binary (here using python syntax)
with open("archive9", "wb") as f:
    f.write(b"2&01")
```

The resultant compressed output is defined in this way: 
<br/>
`<∆ iterations><character_delimiter><final_output_from_last_triangle_iteration_in_triangle_syntax>`
<br/>

The `<character_delimiter>` is, at this time, always provided as the `&` char. There is no particular reason for this
choice, other than the author's delight over Rust's precise
[borrow syntax](https://doc.rust-lang.org/rust-by-example/scope/borrow.html).

## Hardware + OS Snapshot

-  Our Test Machine's [Geekbench5 Score](https://browser.geekbench.com/v5/cpu/16402194)

- SIMD (Single Instruction Multiple Data) available on the listed judge's CPU:
  - https://browser.geekbench.com/user/280257
    - https://browser.geekbench.com/v5/cpu/15864122

## Installation
Download the Linux binaries from the 'Releases' tab.

- Linux: comp9 \[x86_64-unknown-linux-gnu\] (Release pending...)

## Usage
`Publish a compression program "comp9" that outputs archive9 given input enwik9`
```
$ ./comp9 -f enwik9 -o archive9
...[wait for compression]...
```

`If archive9 is run with no input, it reproduces 10**9 byte file data9 that is identical to enwik9`
```
$ ./archive9
...[wait for expansion]...
$ md5sum data9 enwik9
e206c3450ac99950df65bf70ef61a12d  data9
e206c3450ac99950df65bf70ef61a12d  enwik9
```

## Dataset Details

Raw `enwik9` utf-8 characters:
```
Total chars  : 997520890
Unique chars : 10800
```

Blink ingested utf-8 characters:
```
Total chars  : 2660055440
Unique chars : 4
```

## ∆ Numbers

### Perfect ∆
```
150 10010110 1001  10   1 0.125
105 01101001 0110  01   0 0.125
```

### TwoBit ∆
```
102 01100110 0101  00  00 0.25
106 01101010 0111 011  01 0.25
149 10010101 1000 100  10 0.25
153 10011001 1010  11  11 0.25
```

### ThreeBit ∆
```
86  01010110 0001 000 000 0.375
89  01011001 0010 001 001 0.375
101 01100101 0100 000 000 0.375
154 10011010 1011 111 111 0.375
166 10100110 1101 110 110 0.375
169 10101001 1110 111 111 0.375
```