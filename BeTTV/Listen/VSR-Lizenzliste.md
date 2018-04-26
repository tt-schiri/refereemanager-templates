subject:	Lizenzliste Verbandsschiedsrichter
subtitle:	BTTV, Saison ${refdata.content.season.title.value}
date:			Stand: <#setting datetime_format="iso"><#setting locale="de"> ${refdata.info.modified?datetime?string["d. MMMM yyyy"]}
filename:	${refdata.content.season.title.value}_BeTTV_VSR-Lizenzliste.mmd

<!--

\footnotesize

\tabulinesep=_.5\parskip^.5\parskip

\begin{longtabu}[l]{@{}>{\RaggedRight}p{.25\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.25\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.07\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.12\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.09\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.17\textwidth}@{}}
		\toprule
		\textbf{\scriptsize Name} & \textbf{\scriptsize Club} & \textbf{\scriptsize Ausb.} & \textbf{\scriptsize Letzte} & \textbf{\scriptsize Nächste} & \textbf{\scriptsize Entzug?} \\
		\midrule
	\endhead
		\midrule
		\multicolumn{6}{@{}r@{}}{\emph{\scriptsize weiter auf der nächsten Seite\dots}}\\
		\bottomrule
	\endfoot
		\bottomrule
	\endlastfoot

<#list selection as referee>
<#if referee?item_parity == "odd" >\rowcolor{Linen}<#else>\rowcolor{white}</#if>
--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.tableName.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><!-- &
--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.member.displayTitle.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><#if referee.reffor??><!--\newline\textsl{--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.reffor.displayTitle.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><!--}--></#if><!-- &
--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.highestTrainingLevel.type.shorttitle.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><!-- &
--><#if referee.lastTrainingUpdate??><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.lastTrainingUpdate.value?date["yyyy-MM-dd"]?string["dd.MM.yyyy"]}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><#else>---</#if><!-- &
--><#if referee.nextTrainingUpdate??><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.nextTrainingUpdate.value?date["yyyy-MM-dd"]?string["yyyy"]}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><#else>---</#if><!-- &
--><#if referee.revokingLicense.value ><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.revokeLicense.reason.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><#else>---</#if><!--
\\
</#list>

\end{longtabu}

-->

**Legende:**

<#list refdata.content.statusType as statustype>
- <#if statustype.mmdmarkupstart??>${statustype.mmdmarkupstart.value}</#if><#if statustype.remark??>${statustype.remark.value}<#else>${statustype.title.value}</#if><#if statustype.mmdmarkupend??>${statustype.mmdmarkupend.value}</#if>
</#list>
