subject:	Kontaktliste Verbandsschiedsrichter
subtitle:	BTTV, Saison ${refdata.content.season.title.value}
date:			Stand: <#setting datetime_format="iso"><#setting locale="de"> ${refdata.info.modified?datetime?string["d. MMMM yyyy"]}
filename:	${refdata.content.season.title.value}_BeTTV_VSR-Kontaktliste.md

<!--

\footnotesize

\tabulinesep=_.5\parskip^.5\parskip

\begin{longtabu}[l]{@{}>{\RaggedRight}p{.25\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.41\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.24\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.07\textwidth}@{}}
		\toprule
		\textbf{\scriptsize Name} & \textbf{\scriptsize Kontakt} & \textbf{\scriptsize Mitglied\newline\textsl{Schiedst für}} & \textbf{\scriptsize Ausb.} \\
		\midrule
	\endhead
		\midrule
		\multicolumn{4}{@{}r@{}}{\emph{\scriptsize weiter auf der nächsten Seite\dots}}\\
		\bottomrule
	\endfoot
		\bottomrule
	\endlastfoot

<#list selection as referee>
<#if referee?item_parity == "odd" >\rowcolor{Linen}<#else>\rowcolor{white}</#if>
--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.tableName.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><!-- &
--><#list referee.phoneNumber as phonenumber><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${phonenumber.displayTitle.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><#sep><!--\newline --></#sep></#list><#if referee.phoneNumber?? && (referee.phoneNumber?size > 0) && referee.EMail?? && (referee.EMail?size > 0) ><!--\mbox{}\newline --></#if><#list referee.EMail as email><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${email.displayTitle.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><#sep><!--\newline --></#sep></#list><!-- &
--><#if referee.member??><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.member.displayTitleShort.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if></#if><#if referee.reffor??><!--\newline\textsl{--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.reffor.displayTitleShort.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><!--}--></#if><!-- &
--><#if referee.status.mmdmarkupstart??>${referee.status.mmdmarkupstart.value}</#if>${referee.highestTrainingLevel.type.shorttitle.value}<#if referee.status.mmdmarkupend??>${referee.status.mmdmarkupend.value}</#if><!--
\\
</#list>

\end{longtabu}

-->

**Legende:**

<#list refdata.content.statusType as statustype>
- <#if statustype.mmdmarkupstart??>${statustype.mmdmarkupstart.value}</#if><#if statustype.remark??>${statustype.remark.value}<#else>${statustype.title.value}</#if><#if statustype.mmdmarkupend??>${statustype.mmdmarkupend.value}</#if>
</#list>
