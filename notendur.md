```bash
sudo groupadd Söludeild
sudo groupadd Forritun
sudo useradd -m -c "Jón Guðmundsson" -G Söludeild -s /usr/bin/bash jon
sudo useradd -m -c "Kristín Baldursdóttir" -G Söludeild -s /usr/bin/bash kristin
sudo useradd -m -c "Sigríður Sturlaugsdóttir" -G Forritun,sudo -s /usr/bin/bash sigridur
sudo useradd -G Forritun -m -c "Konráð Guðmundsson" -s /usr/bin/zsh konrad
```
