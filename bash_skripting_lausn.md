# Dæmi um lausnir á *Æfingaverkefni í forritun með bash*

## 1a

```bash
#!/usr/bin/bash

read -p "Sláðu inn tölu a: " a
read -p "Sláðu inn tölu b: " b
echo "a + b = $(($a + $b))"
```

## 1b

```bash
#!/bin/bash

read -p "Sláðu inn tölu a: " a
read -p "Sláðu inn tölu b: " b

echo "Aðgerðir:"
echo "1: a + b"
echo "2: a - b"

read -p "Veldu aðgerð: " val

case $val in
    1)
        echo "a + b = $(($a + $b))"
        ;;
    2)
        echo "a - b = $(($a - $b))"
        ;;
    *)
        echo "Skil ekki: $val"
esac    
```

## 1c

```bash
#!/usr/bin/bash

read -p "Sláðu inn tölu a: " a
read -p "Sláðu inn tölu b: " b

val=0

while [ $val -ne 5 ]
do
    echo "Aðgerðir:"
    echo "1: a + b"
    echo "2: a - b"
    echo "3: a * b"
    echo "4: a / b"
    echo "5: Hættta"

    read -p "Veldu aðgerð: " val

    case $val in
        1)
            echo "a + b = $(($a + $b))"
            ;;
        2)
            echo "a - b = $(($a - $b))"
            ;;
        3)
            echo "a * b = $(($a * $b))"
            ;;
        4)
            if [ $b -ne 0 ]
            then 
                echo "a / b = $(($a / $b))"
            else
                echo "b má ekki vera núll!"
            fi
            ;;
        5)
            echo "Takk fyrir!"
            ;;
        *)
            echo "Skil ekki: $val"
    esac  
done
```

## 2a

```bash
#!/usr/bin/bash

read -p "Hvaða sveitarfélag viltu skoða: " sveitarfelag
grep $sveitarfelag ./fakenames.csv | wc -l
```

## 2b

```bash
#!/usr/bin/bash

read -p "Hvaða sveitarfélag viltu skoða: " sveitarfelag
ibuar=$(grep $sveitarfelag fakenames.csv | wc -l | tr -d ' ')
echo "Í sveitarfelaginu $sveitarfelag eru $ibuar skráðir."
```

## 2c

```bash
#!/usr/bin/bash

ibuar=$(grep $1 fakenames.csv | wc -l | tr -d ' ')
echo "Í sveitarfelaginu $1 eru $ibuar skráðir."
```

## 3a

```bash
#!/usr/bin/bash

for i in {1..10}
do
    echo "$i * $1 = $(($i * $1))"
done
```

## 3b

```bash
#!/usr/bin/bash

if [ $1 -eq 0 ]
then
    for i in {1..10}
    do
        for j in {1..10}
        do
            echo -en "$(($i * $j)) \t"
        done
        echo
    done
else
    for i in {1..10}
    do
        echo "$i * $1 = $(($i * $1))"
    done
fi
```

## 4a

```bash
#!/usr/bin/bash

tilraunir=1
slembitala=$((1 + $RANDOM % 100))

read -p "Ég hugsa mér tölu á milli 1 og 100, reyndu að giska á hver hún er: " gisk
while [ $gisk -ne $slembitala ]
do
    if [ $gisk -gt $slembitala ] 
    then
        read -p "Ekki rétt, of há tala, reyndu aftur: " gisk
    else
        read -p "Ekki rétt, of lág tala, reyndu aftur: " gisk
    fi
    tilraunir=$(($tilraunir + 1))
done

echo "Til hamingju þú fannst töluna $slembitala í $tilraunir. tilraun!"
```

## 4b

```bash
#!/usr/bin/bash

tilraunir=1
slembitala=$((1 + $RANDOM % 100))

read -p "Hvað heitir þú? " nafn
read -p "Ég hugsa mér tölu á milli 1 og 100, reyndu að giska á hver hún er: " gisk

if [ $nafn == "ÞITT_NAFN" ]
then
    slembitala=$gisk
fi
while [ $gisk -ne $slembitala ]
do
    if [ $gisk -gt $slembitala ] 
    then
        read -p "Ekki rétt, of há tala, reyndu aftur: " gisk
    else
        read -p "Ekki rétt, of lág tala, reyndu aftur: " gisk
    fi
    tilraunir=$(($tilraunir + 1))
done

echo "Til hamingju $nafn, þú fannst töluna $slembitala í $tilraunir. tilraun!"
```