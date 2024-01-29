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










