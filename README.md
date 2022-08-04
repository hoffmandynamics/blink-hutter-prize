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
