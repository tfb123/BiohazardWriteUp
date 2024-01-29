# BiohazardWriteUp
nmap -sC -sV (IP)

21 tfp

22 ssh

80 http

# The nightmare begin
#July 1998, Evening
The ###STARS alpha team###, Chris, Jill, Barry, Weasker and Joseph is in the operation on searching the STARS bravo team in the nortwest of Racoon city. Unfortunately, the team was attacked by a horde of infected zombie dog. Sadly, Joseph was eaten alive. The team decided to run for the nearby mansion and the nightmare begin..........

Mansion_front.jpg has passphrase(need to be open)

gobuster dir -u http://10.10.145.213 -w /usr/share/wordlists/dirb/common.txt 

/attic, /ccs, /images, /js.

# Main hall
From inspect element we have this info:  It is in the /diningRoom/ 

Mainhall12.jpg has passphrase too(need to be open)

# Dining room
maxresdefault.jpg has passphrase too(need to be open)

Inspect element the page shows us: SG93IGFib3V0IHRoZSAvdGVhUm9vbS8= (base64: How about the /teaRoom/)

http://10.10.145.213/diningRoom/emblem.php - emblem{fec832623ea498e20bf4fe1821d58727}

http://10.10.161.5/diningRoom/sapphire.html (from /diningRoom2F)

blue_jewel{e1d457e96cac640f863ec7bc475d48aa} 

Putting gold_emblem from Bar room reveals: klfvg ks r wimgnd biz mpuiui ulg fiemok tqod. Xii jvmc tbkg ks tempgf tyi_hvgct_jljinf_kvc

So it was vigene cipher: there is a shield key inside the dining room. The html page is called the_great_shield_key

shield_key{48a7a9227cd7eb89f0a062590798cbac}

# Team room
reheader.jpg has passphrase too(need to be open)

Barry also suggested that Jill should visit the /artRoom/

lock_pick{037b35e2ff90916a9abf99129c8e1837}

# Art room

25-image21.jpg has passphrase too(need to be open)

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

16-Image33-1.jpg

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

HEX = c3M6IHlvdV9jYW50X2h(3rd crest decoded)

Hint 1: Crest 3 has been encoded three times

Hint 2: Crest 3 contanis 19 letters

Note: You need to collect all 4 crests, combine and decode to reavel another path

The combination should be crest 1 + crest 2 + crest 3 + crest 4. Also, the combination is a type of encoded base and you need to decode it






















