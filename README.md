# BiohazardWriteUp
nmap -sC -sV (IP)

21 tfp

22 ssh

80 http

# The nightmare begin
#July 1998, Evening
The ###STARS alpha team###, Chris, Jill, Barry, Weasker and Joseph is in the operation on searching the STARS bravo team in the nortwest of Racoon city. Unfortunately, the team was attacked by a horde of infected zombie dog. Sadly, Joseph was eaten alive. The team decided to run for the nearby mansion and the nightmare begin..........

gobuster dir -u http://10.10.145.213 -w /usr/share/wordlists/dirb/common.txt 

/attic, /ccs, /images, /js.

# Main hall
From inspect element we have this info:  It is in the /diningRoom/ 

# Dining room

Inspect element the page shows us: SG93IGFib3V0IHRoZSAvdGVhUm9vbS8= (base64: How about the /teaRoom/)

http://10.10.145.213/diningRoom/emblem.php - emblem{fec832623ea498e20bf4fe1821d58727}

http://10.10.161.5/diningRoom/sapphire.html (from /diningRoom2F)

blue_jewel{e1d457e96cac640f863ec7bc475d48aa} 

Putting gold_emblem from Bar room reveals: klfvg ks r wimgnd biz mpuiui ulg fiemok tqod. Xii jvmc tbkg ks tempgf tyi_hvgct_jljinf_kvc

So it was vigene cipher: there is a shield key inside the dining room. The html page is called the_great_shield_key

shield_key{48a7a9227cd7eb89f0a062590798cbac}

# Tea room

Barry also suggested that Jill should visit the /artRoom/

lock_pick{037b35e2ff90916a9abf99129c8e1837}

# Art room
A map: Location:
/diningRoom/
/teaRoom/
/artRoom/
/barRoom/
/diningRoom2F/
/tigerStatusRoom/
/galleryRoom/
/studyRoom/
/armorRoom/
/attic/

# Bar room
moonlight sonata: NV2XG2LDL5ZWQZLFOR5TGNRSMQ3TEZDFMFTDMNLGGVRGIYZWGNSGCZLDMU3GCMLGGY3TMZL5 (check)

Sonata reveals: music_sheet{362d72deaf65f5bdc63daece6a1f676e}

gold_emblem{58a8c41a9d08b8a4e38d02a4d7ff4843}

Putting emblem reveals nickname: rebecca


# Dining room 2F

Solve this: Lbh trg gur oyhr trz ol chfuvat gur fgnghf gb gur ybjre sybbe. Gur trz vf ba gur qvavatEbbz svefg sybbe. Ivfvg fnccuver.ugzy (Caesar cipher<rot13>)

Solve this: You get the blue gem by pushing the status to the lower floor. The gem is on the diningRoom first floor. Visit sapphire.html (Caesar cipher<rot13>)

# Gallery room

note.txt

crest 2:

GVFWK5KHK5WTGTCILE4DKY3DNN4GQQRTM5AVCTKE

From Base 32 = 5KeuGWm3LHY85cckxhB3gAQMD --> From Base 58 = h1bnRlciwgRlRQIHBh (2nd crest decoded)

Hint 1: Crest 2 has been encoded twice

Hint 2: Crest 2 contanis 18 letters

Note: You need to collect all 4 crests, combine and decode to reavel another path

The combination should be crest 1 + crest 2 + crest 3 + crest 4. Also, the combination is a type of encoded base and you need to decode it

# Tiger status room
crest 1:

S0pXRkVVS0pKQkxIVVdTWUpFM0VTUlk9

From Base 64 = KJWFEUKJJBLHUWSYJE3ESRY --> From base 32 = RlRQIHVzZXI6IG (1st crest decoded)

Hint 1: Crest 1 has been encoded twice

Hint 2: Crest 1 contanis 14 letters

Note: You need to collect all 4 crests, combine and decode to reavel another path

The combination should be crest 1 + crest 2 + crest 3 + crest 4. Also, the combination is a type of encoded base and you need to decode it

# Armor room entrance

crest 3:

MDAxMTAxMTAgMDAxMTAwMTEgMDAxMDAwMDAgMDAxMTAwMTEgMDAxMTAwMTEgMDAxMDAwMDAgMDAxMTAxMDAgMDExMDAxMDAgMDAxMDAwMDAgMDAxMTAwMTEgMDAxMTAxMTAgMDAxMDAwMDAgMDAxMTAxMDAgMDAxMTEwMDEgMDAxMDAwMDAgMDAxMTAxMDAgMDAxMTEwMDAgMDAxMDAwMDAgMDAxMTAxMTAgMDExMDAwMTEgMDAxMDAwMDAgMDAxMTAxMTEgMDAxMTAxMTAgMDAxMDAwMDAgMDAxMTAxMTAgMDAxMTAxMDAgMDAxMDAwMDAgMDAxMTAxMDEgMDAxMTAxMTAgMDAxMDAwMDAgMDAxMTAwMTEgMDAxMTEwMDEgMDAxMDAwMDAgMDAxMTAxMTAgMDExMDAwMDEgMDAxMDAwMDAgMDAxMTAxMDEgMDAxMTEwMDEgMDAxMDAwMDAgMDAxMTAxMDEgMDAxMTAxMTEgMDAxMDAwMDAgMDAxMTAwMTEgMDAxMTAxMDEgMDAxMDAwMDAgMDAxMTAwMTEgMDAxMTAwMDAgMDAxMDAwMDAgMDAxMTAxMDEgMDAxMTEwMDAgMDAxMDAwMDAgMDAxMTAwMTEgMDAxMTAwMTAgMDAxMDAwMDAgMDAxMTAxMTAgMDAxMTEwMDA=

If ends with = then its base

Base 64 = Binary

Binary = HEX

HEX = c3M6IHlvdV9jYW50X2h (3rd crest decoded)

Hint 1: Crest 3 has been encoded three times

Hint 2: Crest 3 contanis 19 letters

Note: You need to collect all 4 crests, combine and decode to reavel another path

The combination should be crest 1 + crest 2 + crest 3 + crest 4. Also, the combination is a type of encoded base and you need to decode it

# Attic

crest 4:

gSUERauVpvKzRpyPpuYz66JDmRTbJubaoArM6CAQsnVwte6zF9J4GGYyun3k5qM9ma4s

From Base 58 = 70 5a 47 56 66 5a 6d 39 79 5a 58 5a 6c 63 67 3d 3d --> From HEX = pZGVfZm9yZXZlcg== (4 crest decoded)

Hint 1: Crest 2 has been encoded twice

Hint 2: Crest 2 contanis 17 characters

Note: You need to collect all 4 crests, combine and decode to reavel another path

The combination should be crest 1 + crest 2 + crest 3 + crest 4. Also, the combination is a type of encoded base and you need to decode it

# Combining crests
We have now 4 crests, COMBINING BEGINS!

RlRQIHVzZXI6IG (1st crest decoded)

h1bnRlciwgRlRQIHBh (2nd crest decoded)

c3M6IHlvdV9jYW50X2h (3rd crest decoded)

pZGVfZm9yZXZlcg== (4 crest decoded)

RlRQIHVzZXI6IGh1bnRlciwgRlRQIHBhc3M6IHlvdV9jYW50X2hpZGVfZm9yZXZlcg== (All combined)

FTP user: hunter, FTP pass: you_cant_hide_forever (Revealed)

# FTP - The guard house

mget *

steghide extract -sf 001-key.jpg

In that key-001.txt we can find this: cGxhbnQ0Ml9jYW

exiftool -a 002-key.jpg

We can find in the comments this: 5fYmVfZGVzdHJveV9

binwalk -e 003-key.jpg --run-as=root

This reveals 3aXRoX3Zqb2x0 inf the folder -> key-003.txt

Lets combine them cGxhbnQ0Ml9jYW5fYmVfZGVzdHJveV93aXRoX3Zqb2x0

From Base 64 = plant42_can_be_destroy_with_vjolt (I assume its a password for the file we downloaded: helmet_ket.txt.gpg

So as i see, we need to install seahorse-nautilus, then open helmet_ket.txt.gpg with the password for it

sudo apt-get install seahorse-nautilus --fix-missing

Then we have this: helmet_key{458493193501d2b94bbab2e727f8db4b}

# Study room entrance

Looking for things in this room we find eagle_medal.txt in the tar.gz

That says: SSH user: umbrella_guest

# Hidden closet

From the file that we downloaded in FTP, we had important.txt info that have /hidden_closet/ room.

From the MO disk 1 we have: wpbwbxr wpkzg pltwnhro, txrks_xfqsxrd_bvv_fy_rvmexa_ajk

weasker login password, stars_members_are_my_guinea_pig | with the key ALBERT

Soo... The Albert Weasker password is: stars_members_are_my_guinea_pig

The wolf medal says: SSH password: T_virus_rules

# SSH

Now we can access SSH: ssh umbrella_guest@10.10.161.5

With the password: T_virus_rules

Check all dirs: ls -la

We can find the .jailcell directory

There is chris.txt file

There is some text and the MO disk 2: albert

Now we can switch to the weasker SSH

su weasker

stars_members_are_my_guinea_pig

Lets try to sudo su with the stars_members_are_my_guinea_pig password

Oops. Now we have the root!

Now we can reach root.txt

flag: 3c5794a00dc56c35f2bf096571edf3bf

It was an amazing adventure and super interesting ctf.














































