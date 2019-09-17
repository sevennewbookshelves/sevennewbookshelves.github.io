# Boeken en andere bronnen:
* [_The tidyverse style guide_](https://style.tidyverse.org/) Werkende code is belangrijk; leesbare code ook. Deze style guide wordt gebruikt door de ontwikkelaars van de tidyverse-packages.
* [_Programming with dplyr_](https://cran.r-project.org/web/packages/dplyr/vignettes/programming.html) Met dplyr is het mogelijk om zeer gemakkelijk door data heen te werken in een onderzoek. Mocht je na deze onderzoeksfase je dplyr-routines zo willen verpakken dat ze later makkelijk te hergebruiken zijn, kijk dan even in dit vignette. Hier wordt uitgelegd hoe je door middel van 'quasiquotation' dplyr-functies flexibel kan toepassen bijv. door `df %>% group_by(!! group_var)` te gebruiken om de group_by-kolom te kunnen variëren.
* Vignettes in het algemeen. Bij een R package is het mogelijk om een demonstratie van het package mee te leveren in de vorm van een 'vignette'. Deze zijn te openen in Rstudio d.m.v. `vignette('package_name')`. Ze staan ook online op de CRAN pagina, bijv. voor [dplyr](https://cran.r-project.org/web/packages/dplyr/index.html).
* [_R Packages_, van Hadley Wickham](http://r-pkgs.had.co.nz/) Het is aan te raden om een idee te krijgen van de opbouw van R packages. Naast dat het een handige, gestandaardiseerde, manier is om je projecten in te delen, geeft het je ook houvast als je in de code van bestaande packages wilt duiken om eens te kijken wat er eigenlijk gebeurd.
* [_Advanced R, 2nd ed._, van Hadley Wickham](https://adv-r.hadley.nz/)([1st ed.](http://adv-r.had.co.nz/)) Voor degene die een beter inzicht willen in hoe R onder de motorkap functioneert en die meer willen doen met R. Er wordt bijvoorbeeld ingegaan op memory management binnen R, het 'copy on modify'-principe (hierdoor zijn for-loops vaak traag in R), object-oriented programming binnen R en het implementeren van C++-code in R via Rcpp voor een grote snelheidsboost als for-loops onvermijdelijk zijn. 
* [GIS in R](http://www.nickeubank.com/gis-in-r/) Een introductie tot GIS in R.

***

# Packages
* [bupaR](http://www.bupar.net/) ([CRAN](https://cran.r-project.org/web/packages/bupaR/index.html)) - Process mining in R. Dit package bevat vele functies die process mining in R erg vergemakkelijken in vergelijking met een aanpak met een data frame en een stel dplyr functies. Bijv. een functie die alle process geeft beginnende met event A en eindigend met event B. 
* KFAS ([CRAN](https://cran.r-project.org/web/packages/KFAS/index.html)) - Tijdreeksanalyse d.m.v. structurele tijdreeksmodellen en state space models. Door middel van het expliciet specificeren van de verschillende componenten van een tijdreeks, bijv. niveau, trend en seizoen, is het mogelijk om accuraat voorspellingen te doen. 


***

# R Snippets
- Bij het werken in grote projecten in Shiny is het handig om code op te delen in [modules](https://shiny.rstudio.com/articles/modules.html). Modules bestaan uit een UI- en een server-deel. Zolang je iedere module voorziet van zijn unieke ID, hoeven alleen nog _binnen_ de module alle input en output IDs uniek te zijn om ervoor te zorgen dat de module goed werkt. [Zie ook hier voor een snippet.](https://gist.github.com/alexanderharms/1f71402d4b703773b65c40367e770c18)