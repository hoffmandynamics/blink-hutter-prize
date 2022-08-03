# blink-hutter-prize
A Hutter Prize submission using 'blink', our selective non-commutative ∆ (triangle) algebra

## Performance - Rust

```
enwik9_char_size :   uncompressed   : compressed :   compression   :      run_time     : improvement
----------------------------------------------------------------------------------------------------
10        chars  : 10         bytes :    6 bytes :   40.00%        :            0.21 s : N          
----------------------------------------------------------------------------------------------------
```

## Performance - Python

```
enwik9_char_size :   uncompressed   : compressed :   compression   :      run_time     : improvement
----------------------------------------------------------------------------------------------------
10        chars  : 10         bytes :    6 bytes :   40.00%        :            7.25 s : N          
100       chars  : 100        bytes :    6 bytes :   94.00%        :            7.14 s : Y          
1000      chars  : 1000       bytes :    7 bytes :   99.30%        :            7.26 s : Y          
10000     chars  : 10001      bytes :    4 bytes :   99.96%        :            7.75 s : Y          
100000    chars  : 100148     bytes :    4 bytes :   99.996%       :           11.76 s : Y          
1000000   chars  : 1004232    bytes :    5 bytes :   99.9995%      :           53.98 s : Y          
10000000  chars  : 10048009   bytes :    4 bytes :   99.99996%     :       8 m 16.49 s : Y          
100000000 chars  : 100379691  bytes :    4 bytes :   99.999996%    :  1 h 48 m 05.22 s : Y          
500000000 chars  :            bytes :      bytes :                 :                   :            
997520891 chars  : 1000000000 bytes :      bytes :                 :                   :            
```

## Geekbench5 Score

- https://browser.geekbench.com/v5/cpu/16402194


## Hardware Snapshot
```
$ neofetch
            .-/+oossssoo+/-.               hdyn@godel 
        `:+ssssssssssssssssss+:`           --------- 
      -+ssssssssssssssssssyyssss+-         OS: Ubuntu 22.04 LTS x86_64 
    .ossssssssssssssssssdMMMNysssso.       Kernel: 5.15.0-41-generic 
   /ssssssssssshdmmNNmmyNMMMMhssssss/      Uptime: 22 hours, 19 mins 
  +ssssssssshmydMMMMMMMNddddyssssssss+     Packages: 2263 (dpkg), 22 (snap) 
 /sssssssshNMMMyhhyyyyhmNMMMNhssssssss/    Shell: zsh 5.8.1 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Resolution: 1920x1080 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   DE: GNOME 42.2 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   WM: Mutter 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   WM Theme: Adwaita 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   Theme: Yaru-blue-dark [GTK2/3] 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Icons: Yaru-blue [GTK2/3] 
 /sssssssshNMMMyhhyyyyhdNMMMNhssssssss/    Terminal: terminator 
  +sssssssssdmydMMMMMMMMddddyssssssss+     CPU: Intel i7-6800K (12) @ 3.800GHz 
   /ssssssssssshdmNNNNmyNMMMMhssssss/      GPU: NVIDIA GeForce GTX 1080 Ti 
    .ossssssssssssssssssdMMMNysssso.       GPU: NVIDIA GeForce GTX 1080 Ti 
      -+sssssssssssssssssyyyssss+-         GPU: NVIDIA GeForce GTX 1080 Ti 
        `:+ssssssssssssssssss+:`           Memory: 48051MiB / 128665MiB 
            .-/+oossssoo+/-.
```
