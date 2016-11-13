---
layout: post
title:  "HTTPs auf alles"
date:   2016-01-18 21:39:00 +0200
image: letsencr.jpg
categories:
- blog
tags:
- https
- letsencrypt
---

Auch bisher war die Verbindung zu den Webseiten des Chaotikums verschlüsselt, die Zertifikate waren allerdings self-signed, was nicht nur weniger Sicherheit garantiert sondern auch für viele Nutzer nervig ist, da sie ihrem Browser immer wieder bestätigen müssen, dass sie der Website vertrauen. Das hat jetzt ein Ende!

Heute hat es eine [Let's Encrypt](https://letsencrypt.org/)-Demonstration im [Nobreakspace](https://chaotikum.org/hackerspace:nbsp) gegeben und nun sind Domains des Chaotikums nicht mehr self-signed, das rote „https“ hat ein Ende.

{% include {{site.image}} base=site.wikiimage url="undefined:letsencr.jpg?w=600&tok=1e1e8f" caption="Console auf und verschlüsseln!" width="655" copyr=site.ccbync %}

Aktuell sind [chaotikum.org](https://chaotikum.org/), [mail.chaotikum.org](https://mail.chaotikum.org/), [pad.chaotikum.org](https://pad.chaotikum.org/) und [cal.chaotikum.org](https://cal.chaotikum.org/) bereits auf Let's Encrypt-Zertifikate umgestellt, weil aber die Anzahl an Zertifikaten pro Woche beschränkt ist werden die anderen Seiten erst nächste Woche ihr TLS-Zertifikat erhalten.

Vom Auflisten aller unserer Domains, über Shell-Skripte und Python-Skripte, bis hin zum erfolgreichen Neustart mit frischen Zertifikaten ist für unsere Infrastruktur alles hier im [pad](https://pad.chaotikum.org/p/letsencrypt) dokumentiert. Ging alles schnell und bequem, und wir empfehlen das Zertifizieren der eigenen Domains auf jeden Fall zum nachmachen!

Wer mehr über Let's Encrypt erfahren möchte, hier ist ein [Talk vom 32C3](https://media.ccc.de/v/32c3-7528-let_s_encrypt_--_what_launching_a_free_ca_looks_like) in dem Roland Bracewell Shoemaker einen kleinen Überblick über die Struktur und Funktionsweise gibt.
