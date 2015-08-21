# Analysis of UseR! 2011 participants by country #
Here is a little example how you can use the `googleVis` package to display the [participants](http://www.warwick.ac.uk/statsdept/useR-2011/participant-list.html) of the [R user conference 2011 in Warwick](http://www.warwick.ac.uk/statsdept/useR-2011/) with a Geo Chart (you could of course use a Geo Map instead):
```
library(XML)
url <- "http://www.warwick.ac.uk/statsdept/useR-2011/participant-list.html"
participants=readHTMLTable(readLines(url), 
             which=1, stringsAsFactors=F)
names(participants)=c("Name", "Country", "Organisation")
## Correct typo and shortcut
participants$Country <- gsub("Kngdom","Kingdom",participants$Country)
participants$Country <- gsub("USA","United States",participants$Country)
participants$Country <- factor(participants$Country)
partCountry <- as.data.frame(xtabs( ~ Country, data=participants))
library(googleVis)
## Please note the option gvis.editor requires googleVis version >= 0.2.9
G <- gvisGeoChart(partCountry,"Country", "Freq", options=list(gvis.editor="Edit me") )
plot(G)
```
&lt;wiki:gadget url="https://docs.google.com/uc?id=0By35Mtg9R9\_RZWUxYTljY2MtNGFlMi00ZjJjLTk3YjgtM2VjYjBjYzJkMTI4&export=download&hl=en\_GB" width="900" height="600" border="0"/&gt;