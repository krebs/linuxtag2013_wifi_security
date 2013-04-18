# Short Abstract
Der Vortrag soll die  Moeglichkeiten von aktuellen OpenWRT-faehigen Routerplattformen im  Bereich Security- und Penetration Testing am Beispiel des TP-Link WR703n vorstellen. Vorgestellt werden auf der Plattform verschiedene Arten von Angriffen auf Wireless-Netzwerke, sowie die  Funktionalitaet als Rogue Access Point in Penetration Tests und als Video und Audio Wanze.
Paper:
# Abstract
Der Vortrag soll die  Moeglichkeiten von aktuellen OpenWRT-faehigen Routerplattformen im  Bereich Security- und Penetration Testing am Beispiel des TP-Link WR703n vorstellen.
In der urspruenglichen Form des lokalen Penetration Tests,welcher sich mit Wireless Networks befasst, ist ein integraler Bestandteil die physikalische Anwesenheit eines Penetration Testers. 
Das  Besondere am WR703n ist die kleine Bauform, geringer Stromverbrauch und sein kostenguenstiger Einsatz. Dies bietet die Moeglichkeit ihn mit einem Akku beliebig zu platzieren und so einen  Angriff auf kabellose Netzwerke auszufuehren ohne physikalisch vor Ort zu sein.  Diese Nutzung eines WR703n als "Dropbox" minimiert sowohl den monetaeren Einsatz als auch die Gefahr beim Penetration Test entdeckt zu werden.
Der Vortrag zeigt  verschiedene Arten von Angriffen auf Wireless-Netzwerke, sowie die  Funktionalitaet als Rogue Access Point in Penetration Tests und als Video und Audio Wanze.
# Einleitung
Der Vortrag soll die Moeglichkeiten von aktuellen openwrt-faehigen Router Plattformen im Bereich Security und Penertration Testing am Beispiel des TP-Link WR703n an praktischen Beispielen vorstellen.
# Die Plattform WR703n
Der TP-Link WR703n ist ein kostenguenstiger Router der sich schon fuer ca 20 Euro importieren laesst. Er besitzt einen USB-Anschluss, welcher urspruenglich dafuer gedacht war ein UMTS-Modem anzuschliessen.  Da er OpenWRT kompatibel ist, kann man viel alternative Software auf dem Router benutzen und der USB-Anschluss bietet quasi endlose Expansionsmoeglichkeiten.
- Technische Stats (400mhz,32mb ram,4mb flash, usb2.0)
( Wir wollen zeigen wie man den WR703n travel-router als Pen-Testing Device mit verschiedenen Anwendungszwecken verwenden kann. (war: Hilfe des WR703n recht einfach in fremde W-Lans eindringen oder fremde Kommunikation belauschen kann). )
# Wifi Penetration Testing 
In der urspruenglichen Form des lokalen Penetration Tests ist ein integraler Bestandteil die physikalische Anwesenheit eines Penetration Testers. 
Das besondere am WR703n ist seine kostenguenstiger Einsatz und dadurch die Moeglichkeit ihn mit einem Akku irgendwo zu platzieren und so den Angriff auszufuehren ohne physikalisch vor Ort zu sein. Diese Nutzung eines WR703 als "Dropbox" minimiert sowohl die monetaere als auch rechtliche Gefahr beim Pen-Testing. Der Vortrag zeigt verschiedene Arten von Angriffen auf Wireless-Netzwerke, sowie die Funktionalitaet als Rogue Access Point in Penetration Tests, sowie als Video und Audio Wanze.
# Bekannte Sicherheitsluecken
## WPS Brute Force
- reaver-wps
## Easybox WPA Password guessing
- link hier
Bei dem Vortrag sollen zwei Live-Hacks gezeigt werden: (echt? ok cool)
    -Knacken eines EasyBox-Standard-WPA Schluessels mit dem TP-Link WR703n
    -Aufsetzen eines Access Points der Seiteninhalte mit Rick-Astley Musik versieht.
Da wir mit dem WR703n im Rahmen unseres Krebs-Projektes arbeiten, werden wir das Krebs-projekt sowie das verteilte VPN Netzwerk "Retiolum"  etwas erlaeutern. 
Die grobe Gliederung des gesammtem Vortrags sieht folgendermassen aus:
Krebs Metaprojekt (was ist Krebs?)
    -Retiolum (vermaschtes Tinc-VPN von Krebs)
-WR703N
    -Hardware (was kann die Hardware, worauf muss man achten)
    -Zubehoer (z.b. USB-Storage, UMTS, Webcam, Batterie)
    -Software (Openwrt, aap-script, wotan.cc Easybox-hack)
-Use-cases
    -MITM (Minikrebs fuer Man-In-The-Middle Angriffe z.b. irgendwo liegen lassen)
        -Tools fuer MITM (aircrack-ng, iptables,dnsmasq, SSL_MITM)
        -Beispiel Rickroller
    -Cracking Wireless/Autoconnecting Wireless
        -Tools fuer Wireless-cracking
            - aap + easybox_hack
            - reaver
        -Remote Cracking (berechnen von WEP/WPA schluessen auf entfernten Rechnern)
    -Ueberwachung (Router mit Webcam oder Mikrofon als Wanze benutzen)
Hi Klaus,
On Fri, Feb 22, 2013 at 11:21:21AM +0100, Justin Otherguy wrote:
> Servus die Herren,
>
> Am 21.02.2013 um 20:08 schrieb Muh Kuh:
>
> > Felix(makefu) und ich(lassulus) wuerden den Vortrag zusammen halten.
> tip-top!
Erstmal Danke fuer die positive Rueckantwort
>
> > Es wuerde hautpsaechlich um die WR703n Router als Pen-Tesing-Device gehen. Speziell die Use-cases als Wireless-cracker und als Honeypoy.
> super; persönlich finde ich die Idee des wireless-crackers am Spannendsten. Den Honeypot kann man dann ja als "Anwendung" oben drauf setzen ("this wps is brought to you by..."  oder so). Vermtl. meint Ihr den Honeypot aber als separate Idee - auch kuhl ("Spass auf Reisen"...).
> (das sind spontane Ideen - die könnt Ihr gerne direkt erden - das ist Euer Vortrag...)
Wir werden dann den fokus auf wireless-cracking legen. Fuer den Vortrag haben wir schon schon ueberlegt eine Mobilen Rick-Roller (honeypot, der auf Ricks video weiterleitet auf basis airbase-ng).
>
> > Das Krebs-Metaprojekt
> die Projektidee habe ich verstanden
>
> > zusammen mit dem Retiolum(tinc-vpn) Darknet
> das nicht - könnt Ihr das in ein paar Worten für mich umreissen?
- ich denke es reicht es anzusprechen, das tinc-vpn ist halt wichtig um die dropboxen im grossen internet wieder zu finden, da das vpn ja den einfachen back-connect ermoeglicht.
>
> > wird von uns auch angesprochen.
> > Der Vortag soll 30minuten dauern.
> ...das wird dann ggf. eng...zielt aber mal auf 30 Min.; ggf. inkl. ein paar Minuten Diskussion.
alles klar, dann planen wir 20-25 minuten vortag ein, wir sind da noch recht flexibel
>
> > Grobe Gliederung des ganzen Vortrags sieht ungefaehr so aus:
> >
> > -Krebs Metaprojekt (was ist Krebs?)
> >    -Retiolum (tinc-netz von Krebs)
> > -WR703N
> >    -Hardware (was kann die Hardware, worauf muss man achten)
> >    -Zubehoer (z.b. USB-Storage, UMTS, Webcam, Batterie)
> >    -Software (Openwrt, aap-script, wotan.cc Easybox-hack)
> > -Use-cases
> >    -MITM (Minikrebs fuer Man-In-The-Middle Angriffe z.b. irgendwo liegen lassen)
> >        -Tools fuer MITM (aircrack-ng, Honeypot, SSL_MITM)
> >        -Beispiel Rickroller
> >    -Cracking Wireless/Autoconnecting Wireless
> >        -Tools fuer Wireless-cracking (aircrack-ng, reaver, aap)
> >        -Remote Cracking (berechnen von WEP/WPA schluessen auf entfernten Rechnern)
> das würde dann schon vorab eine Internetverbindung voraussetzen; als Tool kommt da dann zB reaver zum Einsatz, korrekt?
> Die CPU des WR703N ist da vermtl. zu schwach, als dass man das auf der Box machen könnte, korrekt?
- reaver laeuft auf den wr703 routern ohne probleme.
> In welcher Größenordnung liegt die Crack-Zeit? Bei welchen Ressourcen (CPU, RAM, Plattenplatz)?
Je nachdem was gecrackt werden soll, Easyboxen sind innerhalb von unter einer sekunde "gehackt". WPS dauert laenger, da unter umstaenden jede pin-kombination ausprobiert werden muss. Da die boxen aber klein genug sind um sie in die hecke zu werfen und mit akku fuer >10h zu befeuern ist dies kein wirkliches Hindernis. 
Das ist halt schon ein grosser unterschied als wenn man 12 stunden mit dem auto vor dem haus sitzt, und darum geht es ja
> Kennt Ihr das:
> http://packetstormsecurity.com/files/120216/Net-War-Reaver-Wrapper.html ?
noch nicht :), fuer den wr703 und speziell fuer AAP muessen wir eh dann noch fuer reaver angepasste skripte schreiben. Dieses skript tut schon ein paar sachen die wir dann einfach so uebernehmen koennen.
>
> >    -Ueberwachung (Router mit Webcam oder Mikrofon als Wanze benutzen)
> kuhl
>
> > Wir wuerden uns freuen wenn der Vortrag angenommen wird.
> ...dazu sollte er als Paper auf alle Fälle beim vCC einreichen: httppiratenpad.de/krebsings://vcc.linuxtag.org/
Alles klar, wie lang muss das paper sein? Soll es unseren Vortrag oder das thema speziell beschreiben? 
Gruesse,
makefu,lassulus
- Krebs Metaprojekt
    - "krebs ist ein soziales Experiment, eine Organisation, das zweit aelteste 
  Softwareprojekt im Shack und viel verteilte infrastruktur."
    - Retiolum Darknet (tinc-vpn)
- Hardware: 
    - TP-Link WR703N Router
    - Batterie
        - Laufzeit 
    - USB-Stick
 - in Pen-Testing als Drop-Box
     - Skripte 
        - AAP  (auto AP - magic connect)
        - AAP extension ( Easybox hack)
        - Tinc VPN als Gateway
        - Reaver WPS
- Pentesting als Honeypot
    - Beispiel Rick-Roller
    - Beispiel Rogue Internet Gateway
        - Plain HTTP 
        - SSLstrip
        - SSL_MITM
- Future:
    - UMTS  + WEP + WPA Hack
    - Solarpanel
http://www.seeedstudio.com/depot/lithium-ion-polymer-battery-pack-6a-p-602.html?cPath=178_183 
Akku 27.50
http://www.seeedstudio.com/depot/lipo-rider-pro-p-992.html?cPath=155 
Akku 14.95
http://www.seeedstudio.com/depot/3w-solar-panel-138x160-p-954.html?cPath=155
Solar Panel 14.90
Krebsplug 22.41
http://wiki.openwrt.org/toh/tp-link/tl-wr703n
http://www.volumerates.com/product/genuine-tp-link-tl-wr703n-150m-11n-mini-wifi-wireless-router-for-instant-wifi-connection-99273
Krebsplug Software v0.01
-automagically connect into open wireless networks
    http://wiki.openwrt.org/doc/techref/uci
    uci set wireless.@wifi-device[0].disabled=0; uci commit wireless; wifi   #turns wifi on
    https://forum.openwrt.org/viewtopic.php?id=22427
        sieht richtig aus: 
            Post #19 beachten
-autostart tinc
    already done
    tinc hat uci features: weiteruntersuchen
-fits on internal space
    noch gegeben
-universal rom file
-turn f#@!%$g LED off
   t
-ap + sta mode gleichzeitig
    https://forum.openwrt.org/viewtopic.php?pid=123888#p123888
    
ssh probleme: https://forum.openwrt.org/viewtopic.php?pid=153724
    dns problem!
    
make backup?
krebsing: new intitate: getting started
-get tinc
-join #krebsco on irc.freenode.net
-deploy your pubkey
-connect to the relevant channel

