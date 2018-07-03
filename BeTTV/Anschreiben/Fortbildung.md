subject: Erinnerung Fortbildung
opening: Hallo ${current.firstName.value},
closing: Gruß,
signature: Ekkart.
filename:	${.now?date?string["yyyy-MM-dd"]}_Fortbildung_${current.fileName.value}.md

<#setting datetime_format="iso"><#setting locale="de">

laut meinen Unterlagen war Deine letzte Ausbildung als ${current.highestTrainingLevel.type.shorttitle.value} am ${current.lastTrainingUpdate.value?date["yyyy-MM-dd"]?string["dd.MM.yyyy"]}.

Das heißt, um Deine Lizenz nicht zu verlieren, müsstest Du eine Fortbildung bis Ende ${current.nextTrainingUpdate.value?date["yyyy-MM-dd"]?string["yyyy"]} absolvieren.

Falls ich eine Fortbildung übersehen habe - gib mir einfach Bescheid.

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
