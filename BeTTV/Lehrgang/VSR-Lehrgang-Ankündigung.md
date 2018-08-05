filename:	VSR-Lehrgang-Ankündigung.md

<#setting datetime_format="iso"><#setting locale="de">
Quotes Language:		german
Base Header Level:	3
latex input:				kleinod-mmd-scrartcl
MyOptions:					author=schiri, font=droid, notitlepage, pagestyle=leer
latex input:				kleinod-mmd-style
Title:							Schiedsrichterlehrgang Saison ${refdata.content.season.title.value}
latex input:				kleinod-mmd-begin-doc

<!-- \maketitle -->

Die Berliner Schiedsrichterinnen und Schiedsrichter suchen Verstärkung.
Vielleicht wäre das was für Dich?

Voraussetzung ist, dass Du mindestens 14 Jahre und Mitglied eines Berliner Tischtennisvereins bist.

Was erwartet Dich?

- Einsätze als Oberschiedsrichterin bzw. Oberschiedsrichter von Bundesliga bis Oberliga
- Einsätze als Schiedsrichterin bzw. Schiedsrichter bei Turnieren in Berlin
- bei Interesse Weiterbildung für nationale und internationale Einsätze

Der nächste Verbandsschiedsrichterlehrgang findet im Januar ${refdata.content.season.endYear.value?string["####"]} statt. Folgende Termine sind wichtig:

<#list refdata.content.otherEvent as event>
<#if (event.type.id == "EventDateType.Training") >
- ${event.displayTitleShort.value}: ${event.firstDay.date.value?date['yyyy-MM-dd']?string['EEEE, dd.MM.yyyy']}<#if event.firstDay.startTime??>, ${event.firstDay.startTime.value}<#if event.firstDay.endTime??> -- ${event.firstDay.endTime.value}</#if> Uhr</#if>
</#if>
</#list>

Die Anmeldung erfolgt beim Verbandsschiedsrichterausschuss (VSRA)

> <vsrausschuss@bettv.de>

Die Kosten für den Lehrgang betragen 15 Euro pro Person und werden traditionell vom Verein übernommen.

Mehr Details findest Du auf den Schiriwebseiten unter

> <http://www.tt-schiri.de/schiri-werden.html>
