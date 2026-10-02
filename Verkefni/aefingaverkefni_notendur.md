# Æfingaverkefni 
## Notendur, hópar og fleira

### 0. Undirbúningur
- SSH server
- Zsh
- ohmyz.sh

### 1. Github SSH key

Settu upp ssh lyklapar á Ubuntu (á VirtualBox/UTM) og tengdu við Github reikninginn þinn. Sjá leiðbeiningar [hér](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux).

### 2. Notendur

Búðu til eftirfarandi notendur:
notendanafn | fullt nafn | heimasvæði | skeljarforrit | lykilorð
--- | --- | :-: | --- | --- 
gylfi | Gylfi Sigurðssonn | já | bash | pass.123
aron | Aron Einar Gunnarsson | já | bash | pass.123

#### Lausn
```bash
sudo useradd -c "Gylfi Sigurðsson" -m -s /bin/bash gylfi
sudo useradd -c "Aron Einar Gunnarsson" -m -s /bin/bash aron
sudo passwd gylfi
sudo passwd aron
```

Hægt að skoða `/etc/passwd` skrána til að staðfesta að notendur hafi verið búnir til.

### 3. Hópar

Búðu til hópana `vikingur` og `landslid` (ath. engin íslenskir stafir).

#### Lausn

```bash
sudo groupadd vikingur
sudo groupadd landslid
```

Hægt að skoða `/etc/group` skrána til að staðfesta að hópar hafi verið búnir til.

### 4. Setja notendur í hópa

Settu notandann `aron` í hópinn `landslid`.
Settu notandann `gylfi` í hópana `landslid` og `vikingur`.

#### Lausn

```bash
sudo usermod -aG landslid aron
sudo usermod -aG landslid,vikingur gylfi
```

Hægt að skoða `/etc/group` skrána til að staðfesta að notendur séu komnir í hópa eða nota `id NOTENDANAFN`.


### 5. Búa til notanda og setja í hóp

Búðu til eftirfarandi notanda og settu hann í rétta hópa um leið og þú býrð hann til:

notendanafn | fullt nafn | heimasvæði | skeljarforrit | lykilorð | aukahópar
--- | --- | :-: | --- | --- | ---
arnar | Arnar Gunnlaugsson | já | zsh | pass.123 | landslid, sudo

#### Lausn

```bash
sudo useradd -c "Arnar Gunnlaugsson" -m -s /bin/zsh -G landslid,sudo arnar
sudo passwd arnar
```

### 6. Prófa innskráningu

Prófaðu að skrá alla notendurna inn og gerðu lagfæringar ef þarf.

#### Lausn

Logga inn í GUI eða með `su - NOTENDANAFN`

### 7. Hverjir er innskráðir

Skráðu tvo notendur inn með ssh frá windows/mac og notaðu svo `w` skipunina til að sjá hverjir eru innskráðir og hvaðan.

