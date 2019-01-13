subject:	VSR-Tagung
subtitle:	Anwesenheitsliste
date:			10. April 2018
filename:	09_Anwesenheitsliste.md

<#assign maxcount = 50 >

<!--

\begin{longtabu}[l]{@{}>{\RaggedRight}p{.05\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.3\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.3\textwidth}@{\hspace{.01\textwidth}}>{\RaggedRight}p{.32\textwidth}@{}}
		\toprule
		\textbf{\small Nr.} & \textbf{\small Name} & \textbf{\small Verein} & \textbf{\small Unterschrift}\\
		\midrule
	\endhead
		\midrule
		\multicolumn{4}{@{}r@{}}{\emph{\footnotesize weiter auf der nächsten Seite\dots}}\\
		\bottomrule
	\endfoot
		\bottomrule
	\endlastfoot

<#list selection as referee>
		${referee?counter} & -->${referee.tableName.value}<!-- & --><#if referee.member??>${referee.member.displayText.value}</#if><#if referee.reffor??> *${referee.reffor.displayText.value}*</#if><!-- & \\
		<#sep>\midrule</#sep>
</#list>

<#if (selection?size + 1) &lt; maxcount>
	<#list (selection?size + 1)..maxcount as count>
			\midrule
			${count} &&& \\
	</#list>
</#if>

\end{longtabu}

-->
