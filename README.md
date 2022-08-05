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

## Hardware + OS Snapshot

-  Our Test Machine's [Geekbench5 Score](https://browser.geekbench.com/v5/cpu/16402194)

- \* We leverage SIMD (Single Instruction Multiple Data) available on the listed *judge's* test machine's CPU
architecture:
  - Intel Documentation: [Judge's Test Machine - CPU Specifications](https://ark.intel.com/content/www/us/en/ark/products/208921/intel-core-i71165g7-processor-12m-cache-up-to-4-70-ghz-with-ipu.html)
  - Intel Core i7-1165G7 2.79GHz
    - SSE
    - AVX

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

## Award
`The prize is awarded as follows:`
- Award = Z×(L-S)/L, where
  - S = new record (size of comp9.exe+archive9.exe+opt),
  - L = previous record for S,
  - Z = amount in prize fund (500'000€)
- Update: L := S, while Z itself does not get reduced.
- Minimum award is 1% of Z.
- Contributions are dealt with in the order of their submission.
- The contribution is subject to public comments for a period of at least 30 days before the prize is awarded.

## Award Calculation
```
#!/bin/python3
l = 115352938  # Current record by Artemiy Margaritov
s = 20117      # Size of comp9 (20112) + archive9 (5)
z = 500000     # Prize fund
award = z*(l-s)/l

print("$" + str(award)[:9] + " ")
$499912.80
```

## Rule Fulfillment
- Publish a compression program comp9.exe that outputs archive9.exe given input enwik9. ✅
- If archive9.exe is run with no input, it reproduces 10^9 byte file data9 that is identical to enwik9. ✅
- Total size is measured as S := length(comp9.exe/zip)+length(archive9.exe). ✅
- Programs must be Windows or Linux (x86 32bit or 64bit) executables. ✅
- Programs must run without input from other sources (files, network, dictionaries, etc.) under Windows or Linux without additional installations. ✅
- Use of standard libraries as for file I/O are allowed. ✅
- Each program must run in less than 70'000/T hours on a machine using at most 10GB RAM and 100GB HDD for temporary files, where T is the machine's Geekbench5 score. No GPU usage. ✅
- In particular they must run on our current test machines, which are as of 2021 (but may change without notice) a Lenovo 82HT Intel Core i7-1165G7 2.79GHz (Windows) with T≈1427 (1 core) and T≈4667 (4 cores) and an AMD Ryzen 7 3.6GHz (Linux) with T=1310 (1 core) and T=8228 (8 cores) ✅
