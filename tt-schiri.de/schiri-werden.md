filename:	schiri-werden.md

<#setting datetime_format="iso"><#setting locale="de">
---
title: Schiri werden
date: ${refdata.info.modified?datetime?string['dd.MM.yyyy']}
---

{% capture thumb %}{% include img.html src='VSR-Lehrgang-Ankündigung.png' title='VSR-Lehrgang-Ankündigung' align='right' %}{% endcapture %}
{% include download.html file='VSR-Lehrgang-Ankündigung.pdf' title = thumb %}
Die Berliner Schiedsrichterinnen und Schiedsrichter suchen Verstärkung.
Vielleicht wäre die Schiedsrichterei auch was für Dich?

Der nächste Lehrgang ist im Januar.
Melde Dich beim {% include link.html target='/personen.html' title='Verbandsschiedsrichterausschuss (VSRA)' %}.
Genaueres findest Du am Ende bei [Formalien](#formalien) oder in der {% include download.html file='VSR-Lehrgang-Ankündigung.pdf' title='Ankündigung (PDF)' %}.


## Ausbildung

Der erste Schritt ist die Ausbildung als Verbandsschiedsrichterin bzw. Verbandsschiedsrichter (VSR).
Die Ausbildung findet einmal im Jahr in Berlin in der Geschäftsstelle des BeTTV, Paul-Heyse-Straße statt, sie dauert zwei Abende und endet mit der theoretischen und praktischen Prüfung zu den Berliner Einzelmeisterschaften.
Zusätzlich gibt es einen freiwilligen praktischen Abend, dessen Termin am ersten theoretischen Abend festgelegt wird.

Wenn Du bei den BEM lieber spielen willst, prüfen wir Dich zu einem anderen Turnier, das machen wir dann persönlich aus.


## Karriere

Jede Schiedsrichterin bzw. jeder Schiedsrichter beginnt als Verbandsschiedsrichterin bzw. Verbandsschiedsrichter, das heißt, schiedst als Oberschiedsrichterin bzw. Oberschiedsrichter (OSR) von Bundes- bis Oberliga und als Schiedsrichterin bzw. Schiedsrichter (SR) bei Berliner Turnieren.

Wenn Du möchtest, kannst Du Dich weiterbilden: als nationale oder internationale Schiedsrichterin bzw. Schiedsrichter.
Dabei unterstützen wir Dich natürlich.
Folgende Stufen gibt es (ganz grob):

1. Verbandsschiedsrichterin bzw Verbandsschiedsrichter (VSR)

	Wirst Du mit der obigen Ausbildung und bist danach sofort einsatzbereit.

2. Nationale Schiedsrichterin bzw. nationaler Schiedsrichter (NSR)

	Wirst Du nach frühestens 2 Jahren VSR-Tätigkeit.
	Du wirst vom Schiedsrichterausschuss nominiert und musst eine dreitägige Ausbildung mit Prüfung in Deutschland absolvieren.

3. Internationale Schiedsrichterin bzw. internationaler Schiedsrichter (IU)

	Wirst Du nach frühestens 2 Jahren NSR-Tätigkeit.
	Du wirst vom Schiedsrichterausschuss nominiert und musst eine Prüfung auf Englisch absolvieren.

## Einsätze

In Berlin musst Du als VSR mit ca. 2--3 Einsätzen als OSR in der Saison rechnen, zusätzlich musst Du bei einem größeren Turnier als SR antreten.

Die Turniertage sind festgelegt, Deine Einsätze bei Punktspielen werden vor der Saison festgelegt, die Termine können jedoch zwischen den Schiedsrichtern getauscht werden, wenn Du an einem Termin nicht kannst.

Geld: für jeden Einsatz gibt es Geld, der genaue Betrag hängt bei Punktspielen von der Liga und vom Anfahrtsweg ab (siehe {% include link.html target='/einsatzinformationen/index.html' title='Einsatzinformationen' %}), bei Turnieren etwas mehr, dort wird nach Stunde bezahlt.


## Formalien

Meldung
: schriftlich, mit Name, Vorname, Verein, Mail-Adresse, ggf. Anschrift und Telefon-Nr. an den {% include link.html target='/personen.html' title='Verbandsschiedsrichterausschuss (VSRA)' %}

Teilnahmegebühr
: 15,- €

<#list refdata.content.otherEvent as event>
<#if (event.type.id == "EventDateType.Training") >
${event.displayTitleShort.value}
: ${event.firstDay.date.value?date['yyyy-MM-dd']?string['EEEE, dd.MM.yyyy']}<#if event.firstDay.startTime??>, ${event.firstDay.startTime.value}<#if event.firstDay.endTime??> -- ${event.firstDay.endTime.value}</#if> Uhr</#if>
</#if>

</#list>

Teilnahmevoraussetzungen
: Mindestalter 14 Jahre, Mitglied in einem Berliner TT-Verein, Einzahlung der Teilnahmegebühr, Anschaffung der Verbandsschiedsrichterkleidung (schwarzes Hemd oder Bluse, graue Hose oder Rock, Turnschuhe) und vorheriges Selbststudium der TT-Regeln -- Teil A und B -- und der Wettspielordnung (WO). Die TT-Regeln und die WO werden jedem Teilnehmer per Post oder per E-Mail zugeschickt.

Erhalt der VSR-Lizenz
: Bestehen der mündlichen, schriftlichen und praktischen Prüfung, Einweisung während eines Herrenspieles (6er-Mannschaft) in der 3. Bundesliga oder Regional- bzw. Oberliga bis zum Ende der laufenden Saison.
