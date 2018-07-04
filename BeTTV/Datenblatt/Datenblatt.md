subject:	Datenblatt
subtitle:	${current.displayTitle.value}
date:			Stand: <#setting datetime_format="iso"><#setting locale="de"> ${refdata.info.modified?datetime?string["d. MMMM yyyy"]}
filename:	${current.fileName.value}.md
options:	notitlepage, noauthor, noemail, nosponsorlogo, pagestyle=leer

<#setting datetime_format="iso"><#setting locale="de">

<!--

	{
		\footnotesize
		\sffamily

		\begin{longtabu}[l]{@{}>{\scriptsize\bfseries}p{.23\textwidth}@{\hspace{.02\textwidth}}p{.75\textwidth}@{}}\savetabu{tablayout}

			\multicolumn{2}{@{}l@{}}{\textbf{Sichtbar für Click-TT, Vereine, DTTB, andere VSR, VSRA}}\\
			\midrule
				Name & -->${current.displayTitle.value}<!--\\
				Ausbildung & -->${current.highestTrainingLevel.type.shorttitle.value} (${current.highestTrainingLevel.type.title.value})<!--\\
				Mitglied bei & -->${current.member.displayText.value}<!--\\
				<#if current.reffor??>Schiedst für & -->${current.reffor.displayText.value}<!--\\</#if>
			\bottomrule
		\end{longtabu}

		\begin{longtabu}[l]{\preamble{tablayout}}

			\multicolumn{2}{@{}l@{}}{\textbf{Sichtbar für Vereine, DTTB, andere VSR, VSRA}}\\
			\midrule
				E-Mail & --><#list current.EMail as email>${email.displayTitle.value}<#sep>; </#sep><#else>---</#list><!--\\
				Telefon & --><#list current.phoneNumber as phonenumber>${phonenumber.displayTitle.value}<#sep>; </#sep><#else>---</#list><!--\\
				Geschlecht & -->${current.sexType.displayText.value}<!--\\
			\bottomrule
		\end{longtabu}

		\begin{longtabu}[l]{\preamble{tablayout}}

			\multicolumn{2}{@{}l@{}}{\textbf{Sichtbar für DTTB, VSRA}}\\
			\midrule
				Geburtstag & --><#if current.birthday?? >${current.birthday.value?date['yyyy-MM-dd']?string['dd.MM.yyyy']}<#else>---</#if><!--\\
			\bottomrule
		\end{longtabu}

		\begin{longtabu}[l]{\preamble{tablayout}}

			\multicolumn{2}{@{}l@{}}{\textbf{Sichtbar für andere VSR, VSRA}}\\
			\midrule
				Status & -->${current.status.title.value}<!--\\
				Nächste Fortbildung & --><#if current.nextTrainingUpdate?? >${current.nextTrainingUpdate.value?date['yyyy-MM-dd']?string['yyyy']}</#if><!--\\
			\bottomrule
		\end{longtabu}

		\begin{longtabu}[l]{\preamble{tablayout}}

			\multicolumn{2}{@{}l@{}}{\textbf{Sichtbar für VSRA}}\\
			\midrule
				VSR-Mitteilungen & --><#if current.EMail?? && (current.EMail?size > 0) >per E-Mail<#if current.docsByLetterCombined.value> und </#if></#if><#if current.docsByLetterCombined.value>per Brief</#if><!--\\
				Adresse & --><#list current.address as address>${address.displayTitle.value}<#sep>; </#sep><#else>---</#list><!--\\
				URL & --><#list current.URL as url>${url.displayTitle.value}<#sep>; </#sep><#else>---</#list><!--\\
				Bevorzugt schiedsen & --><#list current.prefer as prefer>${prefer.displayText.value}<#sep>; </#sep><#else>---</#list><!--\\
				Nicht schiedsen & --><#list current.avoid as avoid>${avoid.displayText.value}<#sep>; </#sep><#else>---</#list><!--\\
				<#list current.trainingLevel as traininglevel>
					-->${traininglevel.type.displayText.value} seit<!-- & --><#if traininglevel.since?? >${traininglevel.since.value?date['yyyy-MM-dd']?string['dd.MM.yyyy']}<#else>---</#if><!--\\
				</#list>
				Letzte Fortbildung & --><#if current.lastTrainingUpdate?? >${current.lastTrainingUpdate.value?date['yyyy-MM-dd']?string['dd.MM.yyyy']}</#if><!--\\
				<#if current.remark??>Anmerkung & -->${current.remark.value}<!--\\</#if>
			\bottomrule
		\end{longtabu}
	}

-->
