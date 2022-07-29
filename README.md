# blink-hutter-prize
A Hutter Prize submission using 'blink', our selective non-commutative ∆ (triangle) algebra

## Performance

```
Informally: ∆ compression

enwik9_char_size : uncompressed_file_size : compressed_file_size : compression_ratio : run_time       : improvement
--------------------------------------------------------------------------------------------------------------------
10        chars  : 10         bytes       : 19  bytes            : ~ 189.99%         :       42.40 µs : N           
100       chars  : 100        bytes       : 21  bytes            : ~ 79.00%          :        1.26 ms : N           
1000      chars  : 1000       bytes       : 383 bytes            : ~ 61.70%          :      103.00 ms : N           
10000     chars  : 10002      bytes       : 13  bytes            : ~ 99.87%          :       10.50 s  : Y           
100000    chars  : 100115     btyes       : 149 bytes            : ~ 99.85%          : 15 m  55.00 s  : Y           
1000000   chars  :                        : pending...
10000000  chars  :                        : pending...
997520891 chars  : 1000000000 bytes       : pending...
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