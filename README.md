# blink-hutter-prize
A Hutter Prize submission using 'blink', our selective non-commutative ∆ (triangle) algebra

## Performance - Rust

```
Testing...
```

## Performance - Python

```
enwik9_char_size :   uncompressed   : compressed :   compression   :   run_time   : improvement
-----------------------------------------------------------------------------------------------
10        chars  : 10         bytes :      bytes :   70.00%        :    459.00 µs : N          
100       chars  : 100        bytes :      bytes :   94.00%        :      4.92 ms : Y          
1000      chars  : 1000       bytes :      bytes :   99.30%        :     53.80 ms : Y          
10000     chars  : 10002      bytes :      bytes :   99.96%        :    436.00 ms : Y          
100000    chars  : 100115     bytes :      bytes :   99.996%       :      4.41 s  : Y          
1000000   chars  :            bytes :      bytes :   99.9995%      :     42.10 s  : Y          
10000000  chars  :            bytes :      bytes :   99.99996%     :    7 m 15 s  : Y          
100000000 chars  :            bytes :      bytes :                 :              :            
500000000 chars  :            bytes :      bytes :                 :              :            
997520891 chars  : 1000000000 bytes :      bytes :                 :              :            
```

## Hardware
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