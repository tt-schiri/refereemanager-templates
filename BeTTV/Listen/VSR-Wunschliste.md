subject:	VSR-Tagung
subtitle:	Wünsche, Vorlieben
date:			10. April 2018
filename:	08_Wunschliste.md

Ihr könnt **Vereine**, **Ligen**, oder **Wochentage** angeben oder ob Ihr eher **Ligaspiele** oder **Turniere** bevorzugt.

<!--

\footnotesize

\tabulinesep=_.5\parskip^.5\parskip

\begin{longtabu}[l]{@{}>{\RaggedRight}p{.25\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.43\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.30\textwidth}@{}}
		\toprule
		\textbf{\scriptsize Name} & \textbf{\scriptsize Bevorzugt schiedsen} & \textbf{\scriptsize Nicht schiedsen}\\
		\midrule
	\endhead
		\midrule
		\multicolumn{3}{@{}r@{}}{\emph{\scriptsize weiter auf der nächsten Seite\dots}}\\
		\bottomrule
	\endfoot
		\bottomrule
	\endlastfoot

<#list selection as referee>
<#if referee?item_parity == "odd" >\rowcolor{Linen}<#else>\rowcolor{white}</#if>
-->${referee.tableName.value}<!-- &
--><#list referee.prefer as prefer>${prefer.displayText.value}<#sep><!--\newline --></#sep></#list><!-- &
--><#list referee.avoid as avoid>${avoid.displayText.value}<#sep><!--\newline --></#sep></#list><!-- \\
</#list>

\end{longtabu}


-->
