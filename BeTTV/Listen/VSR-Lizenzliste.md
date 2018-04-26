subject:	Lizenzliste Verbandsschiedsrichter
subtitle:	BeTTV, Saison ${refdata.content.season.title.value}
date:			Stand: <#setting datetime_format="iso"><#setting locale="de"> ${refdata.info.modified?datetime?string["d. MMMM yyyy"]}
filename:	BeTTV_VSR-Lizenzliste.md

<#list refdata.content.statusType as statustype>

# ${statustype.displayTitleShort.value}

<#if statustype.mmdmarkupstart??>${statustype.mmdmarkupstart.value}</#if>${statustype.displayTitle.value}<#if statustype.mmdmarkupend??>${statustype.mmdmarkupend.value}</#if>

<#assign ref_array = [] />
<#list selection as referee>
	<#if (statustype.id == referee.status.id) >
		<#assign ref_array = ref_array + [referee] />
	</#if>
</#list>

<#list ref_array>

<!--

\footnotesize

\tabulinesep=_.5\parskip^.5\parskip

\begin{longtabu}[l]{@{}>{\RaggedRight}p{.25\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.43\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.07\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.12\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.09\textwidth}@{}}
		\toprule
		\textbf{\scriptsize Name} & \textbf{\scriptsize Club} & \textbf{\scriptsize Ausb.} & \textbf{\scriptsize Letzte} & \textbf{\scriptsize Nächste} \\
		\midrule
	\endhead
		\midrule
		\multicolumn{5}{@{}r@{}}{\emph{\scriptsize weiter auf der nächsten Seite\dots}}\\
		\bottomrule
	\endfoot
		\bottomrule
	\endlastfoot

<#items as referee>

<#if referee?item_parity == "odd" >\rowcolor{Linen}<#else>\rowcolor{white}</#if>
-->${referee.tableName.value}<!-- &
--><#if referee.member??>${referee.member.displayTitle.value}<#else>---</#if><#if referee.reffor??><!--\newline\textsl{-->${referee.reffor.displayTitle.value}<!--}--></#if><!-- &
-->${referee.highestTrainingLevel.type.shorttitle.value}<!-- &
--><#if referee.lastTrainingUpdate??>${referee.lastTrainingUpdate.value?date["yyyy-MM-dd"]?string["dd.MM.yyyy"]}<#else>---</#if><!-- &
--><#if referee.nextTrainingUpdate??>${referee.nextTrainingUpdate.value?date["yyyy-MM-dd"]?string["yyyy"]}<#else>---</#if><!--
\\

</#items>

\end{longtabu}

-->

<#else>

Keine VSR.

</#list>

</#list>
