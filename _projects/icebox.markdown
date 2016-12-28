---
layout: project
name:  "Icebox"
date:   2016-06-20 00:00:00 +0200
image: icebox.jpg
tag: icebox
contact:
- "@HerrStachel"
- "@TVLuke"
status: produktiv
short: "Die IceBox ist die digitale Strichliste des Kühlschranks."
categories:
- project
tags:
- icebox
---
Die IceBox ist die digitale Strichliste des Kühlschranks.

Die Icebox findet sich (solange man im nbsp-Netzwerk ist) unter [icebox.nobreakspace.org](http://icebox.nobreakspace.org) die API des Dienstes unter [icebox.nobreakspace.org:8081](http://icebox.nobreakspace.org:8081)

[Aktueller Getränkebestand](https://chaotikum.org/projekte:icebox:icebox_bestand)

## F.A.Q. ##
### Warum das alles? ###
Das System erlaubt es dem Getränkeverantwortlichen zu sehen wann es notwendig ist, eine neue Bestellung aufzugeben und welche Getränke bestellt werden sollten. Es erlaubt dem Kassenwart des Vereins festzustellen welche Aktiva/Passiva wir in Form von Getränken oder Prepaid-Guthaben vorliegen (Dies ist für eine ordnungsgemäße Finanzbuchhaltung relevant).

Zudem erlaubt das System (lustige) Experimente mit Ein- und Ausgabetechniken und Informationsverarbeitung und hilft damit die Umsetzung der Aufgabe des Vereins voranzutreiben. Durch die Abschaffung von Papierlisten für Prepaid-Guthaben schonen wir die Umwelt und sparen Zeit.

### Muss ich einen Account haben? ###
Nein, du kannst das Getränk Anonym kaufen, dann kostet es dich 1.5 € anstelle von 1.25 €. *Warum? Dies ist ein Vereinsbeschluss und hat mit dem System nichts zu tun, es setzt diese Vorgabe lediglich um.*

### Ich habe das falsche Getränk/auf den falschen Account gekauft? ###
Auf dem Touch-Client gibt es 10 Sekunden Undo danach hilft nur miteinander reden, wenn du fälschlicherweise einen Fremd-Account belastet hast. Wenn du das falsche Getränk gekauft hast ist das halb so wild, ab und zu wird Inventur (mehr zur Inventur unten) gemacht und dabei der Bestand korrigiert, das geht auf [icebox.nobreakspace.org](http://icebox.nobreakspace.org/), du kannst es auch gerne jederzeit machen.

### Bleibt mein Guthaben für immer? ###
Nein, Guthaben können nach einem Jahr verfallen, wenn sie nicht genutzt wurden. *Warum? Dies ist ein Vereinsbeschluss und hat mit dem System nichts zu tun, es setzt diese Vorgabe lediglich um.*

### Kann ich digital bezahlen (Überweisung, Paypall…)? ###
Nein, Icebox basiert auf Vertrauen. Du sagst, was du bezahlt hast, Icebox glaubt dir. *Warum? Dies ist ein Vereinsbeschluss und hat mit dem System nichts zu tun, es setzt diese Vorgabe lediglich um.*

### Mein Name taucht auf dem Touchscreen nicht auf obwohl ich mich registriert habe? ###
Kann es sein, dass du kein Guthaben hast? Dann wird dein Name unter den Namen von Nutzern mit Guthaben angezeigt. Wenn du auf deinen Namen drückst bekommst du die Gelegenheit deinen Account mit Guthaben zu versorgen.

###Ein Getränk taucht im System auf aber nicht im Kühlschrank. Was tun?###
Wenn du Glück hast ist das Getränk nur nicht im Kühlschrank aber im Lager (das ist rechts neben dem Kühlschrank), nehme es dir gerne von dort. Wenn da auch keines ist, hat wohl jemand mal einen Fehler beim Verbuchen gemacht und das Getränk ist in Wirklichkeit nicht mehr da, das kann schon mal vorkommen. Du kannst den Fehler unter [icebox.nobreakspace.org](http://icebox.nobreakspace.org/) im Menü unter „Inventur“ (mehr zur Inventur unten) korrigieren, indem du den Bestand für das Getränk auf „0“ setzt, danke.

### Der Barcode an der Flasche funktioniert beim Scannen nicht. ###
Bei einigen Getränken ist der Barcode auf der Flasche nicht (mehr) der selbe wie im System. Die Barcodes am Kühlschrank (gelbe Schilder) funktionieren, der Touchscreen auch. Ob und wann Barcodes angepasst werden hängt von denen ab, die es verbessern, das kannst auch du sein. Ein neues Getränk mit korrektem Barcode kann jeder unter [icebox.nobreakspace.org](http://icebox.nobreakspace.org/) im Bereich „Inventur“ (mehr zur Inventur unten) erstellen, wie ein **neues gelbes Schild** gedruckt werden kann ist unten auf dieser Seite beschrieben.

### Mein Guthaben ist Falsch, wie kann ich es korrigieren? ###
Du kannst dein Guthaben mit einem PUT-Request korrigieren. Wie das geht ist in der API-Doku ([http://docs.iceboxservice.apiary.io/](http://docs.iceboxservice.apiary.io/)) im Detail beschrieben. Je nach Client-Implementierung kann dies auch darüber möglich sein, dies fällt nicht in den Scope des Serverdienstes.

### Wo kann ich ein Problem melden? ###
Für alles, auch Probleme die nicht zwangsläufig etwas mit Code zu tun haben bitte das [Issue System auf Github](https://github.com/Chaotikum/icebox-service/issues) nutzen. Mails oder „im Space bescheid sagen“ gehen leider doch recht schnell unter.

## Known Issues ##
### NoScript unter Firefox ###
Tut nicht. Auch wenn man alles erlaubt. Das ist doof, aber Fakt. Wir sagen, das ist die Schuld des Plugins.

## Software ##
### Clients ###
 * Webclient unter [icebox.nobreakspace.org](http://icebox.nobreakspace.org/)
 * Touch-client auf dem Pi am Kühlschrank ([Github](https://github.com/MotieDesign101/IceBoxTouch))
 * Android [https://github.com/malteschmitz/icebox-android](https://github.com/malteschmitz/icebox-android)
### Dienste ###
 * Die Icebox twittert unter [NbspIcebox](https://twitter.com/NbspIcebox) ([Code auf Github](https://github.com/MotieDesign101/IceBox-Twitter))
 * Es gibt einen Monitoringdienst, der den Bestand aufzeichnen lässt
 * Alias [https://github.com/MotieDesign101/iceBoxAlias](https://github.com/MotieDesign101/iceBoxAlias)
## API-Doku ##
 * [http://docs.iceboxservice.apiary.io/](http://docs.iceboxservice.apiary.io/)
## Inventur ##
Nachdem der Getränkelieferant da war ist es sinnvoll eine Inventur durchzuführen, dabei **sollte** sowohl die **Anzahl der vorhandenen Getränke um die eingekaufte Menge erhöht** werden (einfach die ausgegraute Zahl + die Neueinkäufe) als auch bei **allen Getränken die Leergutmenge auf 0** gesetzt werden.

Inventur ist unter [icebox.nobreakspace.org](http://icebox.nobreakspace.org/) möglich, einfch den in Menü befindlichen Link „Inventur“ nutzen. Dort das Getränk auswählen und die korrekte Information angeben. Felder die nicht verändert werden sollen einfach so belassen wie sie sind.

Neue Getränke können in der selben Maske unten angegeben werden. Es ist aktuell nicht ohne weiteres Möglich ein Bild für ein neues Getränk hinzuzufügen. Als Baarcode sollte der auf der Flasche abgedruckte Baarcode genutzt werden sofern vorhanden. Um neue Schilder zu drucken befindet sich weiter unten ein Link zur entsprechenden tex-Datei.

## Alias anlegen ##
Getränke und User können sich Aliase anlegen. Dies geschieht unter

 icebox.nobreakspace.org:8085/alias

per PUT mit

<code class="javascript">
{
"input": "123456789",
"alias": "tvluke"
}
</code>

Kann man einen registrieren. Wenn man nun GET auf *icebox.nobreakspace.org:8085/alias/123456789* macht so erhällt man

<code class="javascript">
{
  "input": "123456789",
  "alias": "tvluke"
}
</code>

zurück. Der Touch-Client am PI nutzt den ALIAS Service, wenn er einen Input bekommt, den er so nicht kennt. Dies kann genutzt werden, wenn sich der Barcode eines Getränks ändert. Registriert man z.B.

<code class="javascript">
{
  "input": "neuer Barcode",
  "alias": "alter Barcode"
}
</code>

So sollte ab jetzt auch der neue Barcode funktionieren, weil er auf den alten gemappt wird.

Genauso kann die UID eines RFID-Chips auf einen username gemappt werden, damit ein User einen NFC-Chip zur Id am System nutzen kann.

## Offene Ideen ##

 * Anbindung von https://coffeestats.org/
 * Statistiken
   * Verbrauchsprojektion
   * Coole Rankings oder Stats als Website
 * Aktiva/Passiva Rechnung für Kassenwart
 * Licht Im Kühlschrank
   * Erhöhte Komplexität: UDP Multicast bei Getränkeauswahl am Touch-Client, Licht-Client kennt Getränkeposition im Kühlschrank.
 * Case für den Touch-Client am Kühlschrank
 * Mobile-App (Bonjour kann man z.B. nutzen, um automatisch beim verbinden mit WLAN die Icebox zu finden)
 * Vorschlagsmodus (personalisiert oder über den Space)
 * Koffeein- oder Zuckersummierung für User (Un-Health-Monitoring/bestenliste)
 * Twitter-Client besser machen
   * Einkaufen via Twitter
   * @NbspIcebox könnte sich mit @DasBein unterhalten oder so
 * Monatlicher IceBox Bericht
   * Wie viele Getränke wurden gekauft
   * Wie viele User sind registriert
   * Wie viele User waren im letzten Monat aktiv
   * Wie viel Guthaben liegt auf den Accounts
   * Welche User verlieren im nächsten Monat wegen „ein Jahr inaktiv“ ihr Geld
   * Welche Getränke waren populär, welche nicht
   * Uhrzeitverteilung des Kaufens
   * ...

## Hardware ##

 * [Barcode Scanner](https://chaotikum.org/hackerspace:basteln:barcodescanner)
 * PI 2
 * [Pi Touch Monitor](https://www.amazon.de/Official-Raspberry-Pi-Touchscreen-Display/dp/B0153406SS/ref=sr_1_2?ie=UTF8&qid=1466570148&sr=8-2&keywords=pi+touch)
 * NFC-Reader: [AMID RFID Multi-Iso Leser mit Tastatur Emulation](https://www.amazon.de/Multi-ISO-Leser-Keyboard-Emulation-ISO14443-ISO15693/dp/B00K5S7F3W/ref=sr_1_1?ie=UTF8&qid=1470059905&sr=8-1&keywords=amid+rfid+multi+iso+leser)

## Präsentationen ##
  * [Erster Freitalk zur Icebox](https://chaotikum.org/_media/projekte:icebox:pra%CC%88sentation.pdf)

## Kühlschrankschilder ##
Die Barcodes werden auf [http://www.abarcode.net/online.aspx](http://www.abarcode.net/online.aspx) ertsellt. Size 20, Zoom 200%, Format: Transparent PNG. Danach das [Schildformat aus dem Github](https://github.com/Chaotikum/chaotikumSchilder).

Schilder, die aktuell nicht im Einsatz sind, finden sich auf dem Kühlschrank beim Touchscreen.
