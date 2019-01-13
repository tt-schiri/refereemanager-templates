subject:	Gültigkeit Verbandsschiedsrichter
subtitle:	BTTV
date:			Stand: <#setting datetime_format="iso"><#setting locale="de"> ${refdata.info.modified?datetime?string["d. MMMM yyyy"]}
filename:	${refdata.content.season.title.value}_BeTTV_VSR-Gültigkeit.md

<!--

\footnotesize

\tabulinesep=_.5\parskip^.5\parskip

\begin{longtabu}[l]{X[2]X|X[2]X}
		\toprule
		\textbf{\scriptsize Name} & \textbf{\scriptsize Lizenz bis} & \textbf{\scriptsize Name} & \textbf{\scriptsize Lizenz bis}\\
		\midrule
	\endhead
		\midrule
		\multicolumn{4}{r}{\emph{\scriptsize weiter auf der nächsten Seite\dots}}\\
		\bottomrule
	\endfoot
		\bottomrule
	\endlastfoot

<#list selection as referee>
<#if referee?index % 2 == 0 ><#if referee?index % 4 == 0 >\rowcolor{Linen}<#else>\rowcolor{white}</#if></#if>
-->${referee.tableName.value}<!-- &
--><#if referee.nextTrainingUpdate??>${referee.nextTrainingUpdate.value?date["yyyy-MM-dd"]?string["31.12.yyyy"]}<#else>---</#if><!--
<#if referee?item_parity == "odd" >&<#else>\\</#if>
<#if (!referee?has_next) && (referee?item_parity == "odd") >&</#if>
</#list>

\end{longtabu}

-->
