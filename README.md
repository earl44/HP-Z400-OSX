# HP-Z400-OSX
HP Z400 OSX 11.x-12.x


A gép amin teszteltem:
Xeon W3550
20GB DDR3 ECC
ASUS Strix RX470

Ami működik:
*CPU - NullCPUPowerManagement.kext
*GPU – OOB
*Ethernet - CatalinaBCM5701Ethernet.kext
*USB - USBInjectAll.kext
*ICH8 (SSD-HDD) - AHCIPortInjector.kext, IOAHCIBlockStorageInjector_v1.0.0_Micky1979.kext

Ami viszont nem működik:
*Audio: semmilyen módon nem bírtam életre kelteni, szerencsére a HDMI audio OOB működik.


(A telepítéshez szükséged lesz egy másik pc-re vagy mac-re.)
 
1, Telepítő létrehozása:
talán a legegyszerűbb az Olarila Torrentek közvetlen kiírása egy pendrive-ra, de istenigazából mind1 hogyan számtalan leírás van a neten egy a lényeg a Clover induljon és az EFI partíció/mappa tartalma pedig  a CLOVER-5132-HP-Z400.zip tartalma legyen.

2, Indítsd el a telepítést és válasz partíciót formázd APFS -re és hagyd hogy telepítse , ha telepítés nem fog 100% végbe menni hibát fog dobni. Nem lényeges indítsuk újra (a gépet és nem a telepítést) és jöhet a következő lépés.

3, //Ha van lehetőség én egy második pendrive-ra telepíteném az Open Core Bootloadert. Ha nincs akkor sincs baj csak mindig majd újra kell rakni a Clovert ha végeztünk az Open Core részel.//
Az OC-0.9.6.... zip tartalmaz egy működő Open Core bootloadert !! Figyelem mivel DEBUG verzió ezért lassú ne ijedj meg légy türelmes!! a menüben válaszd ki a már HDD/SSD -re telepített OSX-et és indítsd el.  A telepítő betölt és elindul, elsőnek ki fog fagyni. Power Gomb hosszan és kikapcs majd újra be. Újra megismételjük és elindítjuk a telepítést. Akkor vagyunk kész ha az Open Core már nem installernek látja a HDD/SSD -t.(3x kell újra indítani)

4, Ha végeztünk és már nem Installer ként látjuk a menüt akkor jöhet vissza a clover boot loader és indítsuk a gépet vele.


OPENCORE

A pendrive-on hozz létre egy min.80MB méretű partíciót és formázd meg FAT-ra.
Másold fel rá a OC-0.9.6-HP-Z400-nousb mappa tartalmát. A LegacyBoot mappában található BootInstall_X64.tool segítségével tedd bootolhatová a pendrive-ot.
Segítség itt: https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install.html#legacy-setup
!!Figyelem az Open Core -al inditott rendszer bár elindul de az USB nem fog müködni.Arra amire mi használjuk pont megefelell mert akkor nincs szükség beavatkozásra alias billentyüzetre és egére.Viszont támogatja az NVRAM update -et amit a clover nem.!!

CLOVER

!!Arra a pendrive-ra telepítsd amire felraktad az OSX telepítőt.!!
Indítsd el a „Clover_r5132.pkg” és válaszd ki a pendrive-ot majd „Customise” és Install Clover in the ESP, Boot Sectors – Install boot0af in MBR. A többi beállítás lényegtelen.
Ha kész akkor egyszerűen mountold az ESP partíciót a pendrive-on és másold fel a „CLOVER-5132-HP-Z400” tartalmát.
