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

## Resource Utilization
```
Pending...
```

## Installation
Please find the binaries in the 'Releases' portion of this GitHub repository. (Binary building in process...)

- Linux: blink_x86_64-unknown-linux-gnu (Pre-release)
- Windows: blink_x86_64-pc-windows-gnu (Building...)

## Usage
`Publish a compression program "comp9" that outputs archive9 given input enwik9`
```
$ ./blink -c -f enwik9 -o archive9
...[wait for compressor]...
```

`If archive9 is run with no input, it reproduces 10**9 byte file data9 that is identical to enwik9`
```
$ ./archive9
...[wait for expansion]...
$ md5sum data9 enwik9
e206c3450ac99950df65bf70ef61a12d  data9
e206c3450ac99950df65bf70ef61a12d  enwik9
```

Also, feel free to read the `--help` output from the command line:
```
$ ./blink_x86_64-unknown-linux-gnu --help
blink 0.1.7
Hoffman Dynamics - August 5th, 2022
A selective ∆ (triangle) compressor and expansion program.

USAGE:
    blink [OPTIONS] --file <FILE_INPUT> --output <FILE_OUTPUT>

OPTIONS:
    -c, --compress                Compress the provided file
    -e, --expand                  Expand the provided file
    -f, --file <FILE_INPUT>       A file to compress or expand
    -h, --help                    Print help information
    -o, --output <FILE_OUTPUT>    File output for blink operation
    -V, --version                 Print version information
```

## Geekbench5 Score

- https://browser.geekbench.com/v5/cpu/16402194


## Hardware + OS Snapshot
```
$ neofetch
            .-/+oossssoo+/-.               hdyn@godel
        `:+ssssssssssssssssss+:`           ---------
      -+ssssssssssssssssssyyssss+-         OS: Ubuntu 22.04 LTS x86_64
    .ossssssssssssssssssdMMMNysssso.       Kernel: 5.15.0-43-generic
   /ssssssssssshdmmNNmmyNMMMMhssssss/      Uptime: 18 hours, 59 mins
  +ssssssssshmydMMMMMMMNddddyssssssss+     Packages: 2268 (dpkg), 22 (snap)
 /sssssssshNMMMyhhyyyyhmNMMMNhssssssss/    Shell: zsh 5.8.1
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Resolution: 1920x1080
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   Terminal: /dev/pts/0
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   CPU: Intel i7-6800K (12) @ 3.800GHz
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   GPU: NVIDIA GeForce GTX 1080 Ti
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   GPU: NVIDIA GeForce GTX 1080 Ti
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   GPU: NVIDIA GeForce GTX 1080 Ti
 /sssssssshNMMMyhhyyyyhdNMMMNhssssssss/    Memory: 3567MiB / 128665MiB
  +sssssssssdmydMMMMMMMMddddyssssssss+
   /ssssssssssshdmNNNNmyNMMMMhssssss/
    .ossssssssssssssssssdMMMNysssso.
      -+sssssssssssssssssyyyssss+-
        `:+ssssssssssssssssss+:`
            .-/+oossssoo+/-.
```
