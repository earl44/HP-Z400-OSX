# HP-Z400-OSX
HP Z400 OSX 11.x-12.x


A gép amin teszteltem:
Xeon W3550
20GB DDR3 ECC
ASUS Strix RX470
3x SDD
2x HDD

(A telepítéshez szükséged lesz egy másik mac-re.)
 
1, Telepítő létrehozása:
talán a legegyszerűbb az Olarila Torrentek közvetlen kiírása egy pendrive-ra, de istenigazából mind1 hogyan számtalan leírás van a neten egy a lényeg a Clover induljon és az EFI partíció/mappa tartalma pedig  a CLOVER-5132-HP-Z400.zip tartalma legyen.

2, Indítsd el a telepítést és válasz partíciót formázd APFS -re és hagyd hogy telepítse , ha telepítés nem fog 100% végbe menni hibát fog dobni. Nem lényeges indítsuk újra (a gépet és nem a telepítést) és jöhet a következő lépés.

3, //Ha van lehetőség én egy második pendrivra telepíteném az Open Core Bootloadert. Ha nincs akkor sincs baj csak mindig majd újra kell rakni a Clovert ha végeztünk az Open Core részel.//
Az OC-0.9.6.... zip tartalmaz egy működő Open Core bootloadert !! Figyelem mivel DEBUG verzió ezért lassú ne ijedj meg légy türelmes!! a menüben válaszd ki a már HDD/SSD -re telepített OSX-et és indítsd el.  A telepítő betölt és elindul, elsőnek ki fog fagyni. Power Gomb hosszan és kikapcs majd újra be. Újra megismételjük és elindítjuk a telepítést. Akkor vagyunk kész ha az Open Core már nem installernek látja a HDD/SSD -t.(3x kell újra inditani)

4, Ha végeztünk és már nem Installer ként látjuk a menüt akkor jöhet vissza a clover boot loader és indítsuk a gépet vele.
