subject: Passivsetzung Deiner Lizenz
opening: Hi ${current.firstName.value},
closing: Gruß,
signature: Ekkart.
filename:	${.now?date?string["yyyy-MM-dd"]}_Passivsetzung_${current.fileName.value}.md

<#setting datetime_format="iso"><#setting locale="de">
Laut meinen Unterlagen war Deine letzte Ausbildung als ${current.highestTrainingLevel.type.shorttitle.value} am ${current.lastTrainingUpdate.value?date["yyyy-MM-dd"]?string["dd.MM.yyyy"]}.
Das heißt, um Deine Lizenz nicht zu verlieren, hättest Du an einer Fortbildung bis Ende ${current.nextTrainingUpdate.value?date["yyyy-MM-dd"]?string["yyyy"]} teilnehmen müssen.

Wir setzen daher Deine Lizenz passiv, das heißt, Du wirst offiziell nicht mehr als VSR an den Verband gemeldet.
Du hast die Chance, Deine Lizenz wieder zu aktivieren, indem Du an einer Fortbildung teilnimmst.

Wenn Du das nicht tust, werden wir Dir die Lizenz Ende der nächsten Saison entziehen.

Falls wir etwas übersehen haben oder wir einfach drüber reden sollen, melde Dich.

Die nächste Fortbildungen sind:

<#assign events = [] />
<#list refdata.content.otherEvent as event>
	<#if (event.type.id == "EventDateType.Update") >
		<#assign events = events + [event] />
	</#if>
</#list>
<#list events as event>
<@compress single_line=true>
- ${event.dateText.valueSafe}<#if event.timeText??>, ${event.timeText.valueSafe} Uhr</#if>
-- ${event.displayTitleShort.value}
</@compress>

</#list>
