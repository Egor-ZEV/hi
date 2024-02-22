uic@teleport:~/Project/cisco$ sudo curl https://goteleport.com/static/install.sh | bash -s 12.2.1
shell-init: error retrieving current directory: getcwd: cannot access parent directories: No such file or directory
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  9759    0  9759    0     0  34216      0 --:--:-- --:--:-- --:--:-- 34242
Installing Teleport v12.2.1 via apt-get
Downloading Teleport's PGP public key...
Downloading https://apt.releases.teleport.dev/gpg
+ sudo curl -fL -o /tmp/teleport-LoyI2IaIwL/teleport-pubkey.gpg https://apt.releases.teleport.dev/gpg
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  3163  100  3163    0     0  11620      0 --:--:-- --:--:-- --:--:-- 11671
+ set +x
+ sudo tee /usr/share/keyrings/teleport-archive-keyring.asc
+ cat /tmp/teleport-LoyI2IaIwL/teleport-pubkey.gpg
+ set +x
+ echo 'deb [signed-by=/usr/share/keyrings/teleport-archive-keyring.asc]  https://apt.releases.teleport.dev/ubuntu jammy stable/v12'
+ sudo tee /etc/apt/sources.list.d/teleport.list
+ set +x
+ sudo apt-get update
Hit:1 http://ru.archive.ubuntu.com/ubuntu jammy InRelease
Hit:2 http://ru.archive.ubuntu.com/ubuntu jammy-updates InRelease                                                                                                                                                 
Hit:3 http://ru.archive.ubuntu.com/ubuntu jammy-backports InRelease                                                                                                                                               
Hit:4 http://packages.microsoft.com/repos/code stable InRelease                                                                                                                                                   
Ign:5 https://repo.yandex.ru/yandex-browser/deb jammy InRelease                                                                                                                                                   
Hit:6 https://repo.yandex.ru/yandex-browser/deb beta InRelease                                                                                                                     
Hit:7 https://repo.yandex.ru/yandex-browser/deb stable InRelease                                                       
Err:8 https://repo.yandex.ru/yandex-browser/deb jammy Release                                    
  404  Not Found [IP: 213.180.204.183 443]
Hit:9 https://apt.releases.teleport.dev/ubuntu jammy InRelease                                   
Get:10 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]                       
Hit:11 https://download.docker.com/linux/ubuntu jammy InRelease            
Reading package lists... Done                             
E: The repository 'https://repo.yandex.ru/yandex-browser/deb jammy Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
