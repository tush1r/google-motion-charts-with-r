**NEWS `[4 July 2015]`:** googleVis 0.5.9 released on CRAN

**`[4 March 2014]`:** The source code development of googleVis moved to [GitHub.](https://github.com/mages/googleVis)

For more details see the [news section](http://code.google.com/p/google-motion-charts-with-r/#News) and check out the [blog for further news and examples](http://lamages.blogspot.com/search/label/googleVis).

Should you find any issues or bugs with this version, then please drop us a line or add them to our [issues list](https://github.com/mages/googleVis/issues).


[![](https://www.paypal.com/en_GB/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=HHPMW8TXCCRSC&lc=GB&item_name=googleVis&currency_code=GBP&bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted)


# Introduction #
`googleVis` is an [R](http://www.r-project.org) package providing an interface between R and [Google Charts](https://developers.google.com/chart/).
The functions of the package allow the user to visualise data with the Google Chart Tools without uploading their data to Google.

The output of `googleVis` functions is html code that contains the data and references to  `JavaScript` functions hosted by Google. To view the output a browser with Flash and Internet  connection is required, the actual chart is rendered in the browser.
<a href='Hidden comment: 
<wiki:gadget url="http://dl.dropbox.com/u/7586336/GoogleVis_London_7_September_2011.xml" frameborder="0" width="410" height="340" />'></a>

![http://3.bp.blogspot.com/-9Pj5EM9bo-E/UdMe7VOA5MI/AAAAAAAAA-c/LBqC-YikDt0/s400/googleVis_tutorial.png](http://3.bp.blogspot.com/-9Pj5EM9bo-E/UdMe7VOA5MI/AAAAAAAAA-c/LBqC-YikDt0/s400/googleVis_tutorial.png)
  * [googleVis Tutorial](http://lamages.blogspot.co.uk/2013/07/googlevis-tutorial-at-user2013.html)
  * [googleVis in the 2011/2 R-Journal](http://code.google.com/p/google-motion-charts-with-r/downloads/detail?name=RJournal_2011-2_Gesmann%2Bde%7ECastillo.pdf)
  * [Video tutorial](http://www.youtube.com/watch?feature=player_embedded&v=Z6NYQdiwTrU) by [Martin Hilpert](http://members.unine.ch/martin.hilpert/motion.html)
  * [Google Chart Tools at Google I/O 2013](https://developers.google.com/events/io/sessions/401719292) by Mitchell Foley
<a href='Hidden comment: 
For a quick start read:
<table>
<tbody>
<tr>
<td>
<wiki:gadget url="http://dl.dropbox.com/u/7586336/GoogleVis_London_7_September_2011.xml" frameborder="0" width="410" height="340" />
* [https://docs.google.com/present/view?id=d43t954_258r33v77cn googleVis at LondonR September 2011]


Unknown end tag for &lt;/td&gt;


<td>
<wiki:gadget url="http://dl.dropbox.com/u/7586336/blogger/pdfviewer.xml" width="410" height="100" border="0"/>
* [http://code.google.com/p/google-motion-charts-with-r/downloads/detail?name=RJournal_2011-2_Gesmann%2Bde%7ECastillo.pdf R Journal 2011 2]


Unknown end tag for &lt;/td&gt;




Unknown end tag for &lt;/tr&gt;




Unknown end tag for &lt;/tbody&gt;




Unknown end tag for &lt;/table&gt;


'></a>
# Examples #
Here is an example of a Motion Chart ([user guide](http://google-motion-charts-with-r.googlecode.com/svn/trunk/vignettes/MotionChart.pdf)) using data from the [World Bank](http://www.worldbank.com):

&lt;wiki:gadget url="http://dl.dropbox.com/u/7586336/googleVisExamples/WorldBankMotionChartFeb2013.xml" width="550" height="420" border="0"/&gt;

You can achieve the same result with the `googleVis` package and [R](http://www.r-project.org) without placing your data on the web. The function `gvisMotionChart` generates the motion chart locally. Please read Google's [Data Policy](https://developers.google.com/chart/interactive/docs/gallery/motionchart#Data_Policy) and [Terms of Use](https://developers.google.com/chart/termsl). The above chart is the output of the demo World Bank. This is how it works:
```
library(googleVis)
demo(WorldBank) ## At least version googleVis_0.2.10 required
```
The output of `gvisMotionChart` contains all the data and a reference to the Google Chart Tools. The actual Flash chart is rendered within the browser. Please see also the package [vignette](http://cran.r-project.org/web/packages/googleVis/vignettes/googleVis.pdf).

You find more **[googleVis examples](http://cran.r-project.org/web/packages/googleVis/vignettes/googleVis_examples.html)** on CRAN and [blog](http://lamages.blogspot.com/search/label/googleVis).

# Motivation #
In 2006 Hans Rosling gave an inspiring talk at [TED](http://www.ted.com/talks/hans_rosling_shows_the_best_stats_you_ve_ever_seen.html) about social and economic developments in the world over the last 50 years, which challenged the views and perceptions of many listeners. Rosling had used extensive data analysis to reach his conclusions.  To visualise his talk, he and his team at [Gapminder](http://www.gapminder.org) had developed animated bubble charts.

Rosling's presentation popularised the idea and use of interactive charts, and as a result the software behind
Gapminder was bought by Google and integrated as motion charts into their [Visualisation API](https://developers.google.com/chart/interactive/docs/index) one year later.

Inspired by those talks and the desire to use interactive data visualisation tools to foster the dialogue between data analysts and others the authors of this page started the development of the googleVis package.

<a href='Hidden comment: 
==Screenshots==
<img src="http://google-motion-charts-with-r.googlecode.com/svn-history/r115/trunk/inst/doc/googleVisDemoPlots.png" width="500" height="500">

* Screenshots of some of the outputs of  demo(googleVis, package="googleVis") with gvisMotionChart, gvisAnnotatedTimeLine, gvisMap, gvisGeoMap, gvisTable and gvisTreeMap from top left to bottom right.
'></a>
# Installation #
In all cases [Flash](http://get.adobe.com/flashplayer) and an internet connection is required to view the visualisation output. Of course you also need [R](http://www.r-project.org). R version 3.0.2 or higher is required for googleVis version >= 0.5.0.

If you are new to R and installing add-on packages please read the [R Installation and Administration manual](http://cran.r-project.org/doc/manuals/R-admin.html).

### From  [CRAN](http://cran.r-project.org/web/packages/googleVis/) ###
Start R on your computer and type:
```
 install.packages('googleVis')
```
## From Github ##

To install the current development version from Github you need the devtools package and the other packages on which googleVis depends:
```
install.packages(c("devtools","RJSONIO", "knitr", "shiny", "httpuv"))
```
To install googleVis run:
```
library(devtools)
install_github("mages/googleVis")
```
## Using googleVis ##
Please read the [Google Terms of Service](https://developers.google.com/chart/terms)  before you use the `googleVis` package.

After you installed the package type into R:
```
 library('googleVis')
```
Type `library(help='googleVis')` or `?googleVis`
to see the overall documentation.  Type `demo(googleVis)` to get an idea of the functionality of the package.

For a brief introduction read the five page [R Journal article](http://google-motion-charts-with-r.googlecode.com/files/RJournal_2011-2_Gesmann%2Bde%7ECastillo.pdf).
# Tips & Tricks #
  * [Using googleVis with WordPress](UsingWordPress.md)
  * [Setting gvis-chart options](SettingOptions.md)
  * [Combing charts with gvisMerge](GvisMerge.md)
  * [Ideas on event listener handlers](ListenerEvents.md)
  * [Displaying a motion chart locally](http://stackoverflow.com/questions/8009825/cannot-view-gvismotionchart-from-printed-html-file)
  * [More tips and tricks are documented in the package vignette](http://cran.r-project.org/web/packages/googleVis/vignettes/googleVis.pdf).

# Presentations #
  * [googleVis Tutorial at useR! 2013](http://lamages.blogspot.co.uk/2013/07/googlevis-tutorial-at-user2013.html) (googleVis 0.4.3)
  * [Introduction to googleVis](http://lamages.blogspot.co.uk/2013/05/interactive-presentation-with-slidify.html), Lancaster University, 21 May 2013 (googleVis 0.4.3)
  * [Interactive web graphs with R - Overview and googleVis tutorial](http://lamages.blogspot.co.uk/2012/09/interactive-web-graphs-with-r-overview.html), RSS Conference, 5 September 2012 (googleVis-0.2.17)
  * [Interactive HTML presentation with R, googleVis and knitr](http://lamages.blogspot.co.uk/2012/05/interactive-html-presentation-with-r.html), Cambridge R users group, 29 May 2012 (googleVis-0.2.16)
  * [Getting started with googleVis](http://dl.dropbox.com/u/7586336/blogger/deck.js/googleVis/index.html) (googleVis-0.2.11)
  * [googleVis at LondonR September 2011](https://docs.google.com/present/view?id=d43t954_258r33v77cn) (googleVis-0.2.9)
  * [googleVis at useR! August 2011](https://docs.google.com/present/view?id=ddcm6vg7_0fjk76xg9) (googleVis-0.2.8)
  * [googleVis at Rmetrics June 2011](https://docs.google.com/present/view?id=d43t954_229g7s9p5nc) (googleVis-0.2.6)
  * [Google Visualisation at LondonR, 5 October 2010](http://google-motion-charts-with-r.googlecode.com/files/GoogleMotionCharts%20MG%20EW%202010Oct5.pdf) (googleVis-0.1.2)
  * R/RMETRICS Generator Tool for Google Motion Charts by Sebastián Pérez Saaibi at the BaselR user group July 2010
  * [Google Visualization API demos and slides presented at Google I/O 2011](http://code.google.com/p/google-visualization-io2011/) (Michael Fink, Riccardo Govoni and Amit Weinstein)
# Case studies #
  * [Statistics Relating to Lloyd's](http://www.lloyds.com/The-Market/Tools-and-Resources/Resources/Statistics-Relating-to-Lloyds/Visualisation)
  * [Analysis of the US domestic airline market from 1999 - 2010](http://www.cambridge.aero/_blog/main/post/US_Domestic_Airline_Market_In_Motion_1990-2010/)
  * [Linguistic analysis of the English language](http://omnibus.uni-freiburg.de/~mh608/motion.html)
  * [Spatial analysis](http://spatialanalysis.co.uk/2011/01/10/r-interface-to-google-chart-tools/)
  * [Ecological analysis](http://r-ecology.blogspot.com/2011/01/r-and-google-visualization-api-fish.html)
  * [Nucelar power analysis](https://sites.google.com/site/rprojectie/)
# Links #
  * [Google Visualisation API](http://code.google.com/apis/visualization/documentation/gallery.html)
  * TED talk: [Hans Rosling shows the best stats you've ever seen](http://www.ted.com/talks/hans_rosling_shows_the_best_stats_you_ve_ever_seen.html)
  * [Gapminder](http://www.gapminder.org) - shows the world’s trends
  * [Google Open Data Explorer](http://www.google.com/publicdata/home) - access to public data
## Other R packages ##
  * [R Server Pages and Light-weight HTTP daemon (server)](http://www.braju.com/R/)
  * [RJSONIO](http://www.omegahat.org/RJSONIO/) reading and writing data in JSON
  * [plotGoogleMaps](http://cran.r-project.org/web/packages/plotGoogleMaps/): Plot HTML output with Google Maps API and your own data
  * [R2GoogleMaps](http://www.omegahat.org/R2GoogleMaps/): Provides a mechanism to generate `JavaScript` code from R that displays data using Google Maps
  * [RgoogleMaps](http://cran.r-project.org/web/packages/RgoogleMaps/index.html): Overlays on Google map tiles in R
  * [R animation package](http://animation.yihui.name/) allows to create SWF, GIF and MPEG directly, e.g. [bubble animation](http://animation.yihui.name/da:ts:hans_rosling_s_talk)
  * [playwith: A GUI for interactive plots using GTK+](http://cran.r-project.org/web/packages/playwith)
  * [iplots: iPlots - interactive graphics for R](http://cran.r-project.org/web/packages/iplots/)
  * [rggobi: Interface between R and GGobi](http://cran.r-project.org/web/packages/rggobi/)
  * [gridSVG: Export grid graphics as SVG](http://cran.r-project.org/web/packages/gridSVG/index.html)
# News #
```
googleVis 0.5.9 [2015-07-04]
----------------------------

Changes

  * Added note section on width and height to help file of 
    gvisIntensityMap. Thanks to Sarang Brahme for his comment.
   
  * Updated NAMESPACE file to comply with new R CMD checks in R-3.3.0   


googleVis 0.5.8 [2015-01-21]
----------------------------

* Internal changes to how the internal web server is called, to reflect
  changes in R 3.2.0


googleVis 0.5.7 [2014-12-20]
----------------------------

Changes

* Updated DESCRPITION file to comply with new CRAN policy

* Clarified setting parameters in help file.
  Thanks to Nick Salkowski for his suggestions.


googleVis 0.5.6 [2014-10-12]
----------------------------

Changes

* Rescaled the column "% of World Population" in sample data set "Population" 
  by a factor of 0.01

Bug Fixes

* gvisMotionChart: arguments xvar, yvar, sizevar and colorvar were not 
  always picked up correctly. 
  Thanks to Juuso Parkkinen for reporting this issue.


googleVis 0.5.5 [2014-08-15]
----------------------------

Changes

* Added example to gvisMerge help file.

Bug Fixes

* README.md when converted to (X)HTML using a current version of 
  pandoc showed minor problems when validated using W3C Markup 
  Validator.

* In some case when no xvar and yvar arguments where provided for 
  core charts the output wasn't sensible. This bug was introduced 
  with version 0.5.3. Thanks to stanstrup for reporting this issue.


googleVis 0.5.4 [2014-07-19]
----------------------------

Changes

* Tidying up of googleVis demo, vignette and README file


googleVis 0.5.3 [2014-06-28]
----------------------------

Changes

* Default chart width is set to 'automatic' instead of 500 pixels.

* Intervals for columns roles have to end with the suffix ".i",
  with i being an integer. Several interval columns are allowed,
  see the Roles demo and vignette for more details.

Bug Fix

* The order of y-variables in core charts wasn't maintained.
  Thanks to John Taveras for reporting this bug.

* Width and height of googleVis charts were only accepted in pixels, 
  although the Google Charts API uses standard HTML units (for
  example, '100px', '80em', '60', 'automatic'). If no units are specified 
  the number is assumed to be pixels. This has been fixed.
  Thanks to Paul Murrell for reporting this issue.


googleVis 0.5.2 [2014-05-05]
----------------------------
Changes

* Fixed minor formatting issues in documentation and vignettes.

* Added examples in demo googleVis to show how to
  customize points and lines and to the help files of
  gvisLineChart and gvisScatterChart.


googleVis 0.5.1 [2014-04-14]
----------------------------
NEW FEATURES

* New functions gvisSankey, gvisAnnotationChart, gvisHistogram,
  gvisCalendar and gvisTimeline to support the new Google charts 
  of the same names (without 'gvis').

* New demo Trendlines showing how trend-lines can be added to
  Scatter-, Bar-, Column-, and Line Charts.

* New demo Roles showing how different column roles can be used
  in core charts to highlight data.

* New vignettes written in R Markdown showcasing googleVis
  examples and how the package works with knitr.

Changes

* The help files of gvis charts no longer show all their options,
  instead a link to the online Google API documentation is given. 

* Updated googleVis demo

* All googleVis output will be displayed in your default browser. 
  In previous versions of googleVis output could also be displayed 
  in the preview pane of RStudio. This feature is no 
  longer available with the current version of RStudio, but is likely to   
  be introduced again with the release of RStudio version 0.99 or higher.


googleVis 0.4.7 [2013-11-10]
----------------------------

Changes

* New option 'googleVis.viewer' which controls the default output of
  the googleVis plot method. On package load it is set to 
  getOption("viewer"). It you use RStudio, then its viewer pane will 
  be used for displaying non-Flash charts. 
  Set options("googleVis.viewer"=NULL) and the googleVis
  plot function will open all output in the default browser again.

* The package start-up message makes the user aware of the default 
  viewer option.

* Added example to gvisMap that illustrates how the icon can be 
  changed.


googleVis 0.4.6 [2013-11-03]
----------------------------

Changes

* googleVis will use the Viewer pane in RStudio (version >= 0.98.441) 
  to display non-Flash charts by default. The setting is controlled
  via the option viewer. Set options("viewer"=NULL) and the googleVis
  plot function will open all output in the default browser again.


googleVis 0.4.5 [2013-08-29]
----------------------------

Bug Fixes

* The indentation of some of the HTML output changed in version 0.4.4,
  which as a result stopped googleVis output to be rendered with knitr.


googleVis 0.4.4 [2013-08-23]
----------------------------

NEW FEATURES

* gvisTable() gained new parameter formats, which allow users to 
  specify the format of numbers displayed in a table. 
  Thanks to Jacqueline Buros for providing ideas and code.

* Doughnut charts are now possible as pie charts with a hole.

Changes

* New examples for gvisBarChart, gvisColumnChart, gvisComboChart 
  demonstrating how to change the width of bars

* Extended FAQ section


googleVis 0.4.3 [2013-05-25]
----------------------------

NEW FEATURES
 
 * givsGeoChart has a new argument 'hovervar' to specify a column in
   input data that can be used to show additional information in a geo
   chart. See the new example of plotting countries' credit rating in
   the help file for a use case. Thanks to John Muschelli for suggesting
   this feature.


googleVis 0.4.2 [2013-03-16]
----------------------------

NEW FEATURES

 * The core charts (e.g. line, area, bar, column and combo charts)
   accept now also date variables for the x-axis. Thanks to Sebastian
   Campbell for pointing this out.

Changes 

 * The WorldBank demo uses now the WDI package.
   Thanks to John Maindonald for providing the code.

Bug Fixes

 * Fixed typos in Stock and Andrew example data. 
   Thanks to Sebastian Campbell for reporting this issue. 


googleVis 0.4.0 [2013-02-24]
----------------------------

NEW FEATURES
 
 * New function renderGvis to support shiny.
   This function allows user to insert googleVis output into shiny
   apps, similar to renderText and renderPlot. See the help page for
   more details. Many thanks to Joe Cheng for his support and help.

Changes

 * In order to support shiny the order of the elements of the
   gvis*()$html$chart vector changed. The positions of jsChart and
   jsFooter have been swapped.

 * The load mechanism for the Google API changed from http to https
   again. Thanks to Jacques Philip. 

 * The package dependencies changed to imports statements in DESCRIPTION. 
   Thanks to Suraj Gupta for pointing this out.

 * The R.rsp example in demo googleVis has been moved into its own
   demo Rrsp. 

 * A FAQ and shiny section has been added to the vignette.

Bug Fixes

 * jsDisplayChart didn't check if the google visualization function is already
   loaded. Many thanks to Mark Melling for reporting the issue and
   providing a solution.

 * The demo WorldBank didn't download all data but only the first
   12000 records. Many thanks to John Maindonald reported this issue. 


googleVis 0.3.3 [2012-11-12]
----------------------------

Changes

 * Clarified the usage of the argument state in the help file of
   gvisMotionChart. Thanks to Leonardo Trabuco 


googleVis 0.3.3 [2012-10-31]
----------------------------

Bug Fixes

 * plot.gvis didn't open a browser window when options(gvis.plot.tag)
   was not set to NULL, but the user explicitly called plot.gvis with
   tag NULL. Thanks to Sebastian Kranz for reporting this bug. 


googleVis 0.3.2 [2012-10-28]
----------------------------

NEW FEATURES

 * plot.gvis gained the argument 'tag', which works similar to the
   argument of the same name in print.gvis. By default the tag
   argument is NULL and plot.gvis has the same behaviour as in the
   previous versions of googleVis. 
   However, the argument can be set outside plot.gvis via
   options(gvis.plot.tag=...). This allows users to switch plot
   statements into print statements by changing only one setting. This
   is particular useful when googleVis is used in combination with
   knitr or R.rsp. Setting options(plot.gvis.tag="chart") will ensure
   that plot(gvisOutput) statements will be included into the final
   HTML output. See the help file to plot.gvis and vignette for more
   details. 

Changes

 * The tag argument of print.gvis can be set globally from outside the
   function via options(gvis.print.tag)

 * The vignette has a new section describing how to set the
   behaviour of plot.gvis and print.gvis via options(gvis.plot.tag),
   options(gvis.print.tag) respectively. The section describing how
   googleVis can be used with knitr has been extended and an additional
   example included. 

 * plot.gvis can open any html file now, not just gvis-objects. Like
   with gvis-object it will copy the file into a temporary directory
   and display it via the R HTTP server. 


googleVis 0.3.1 [2012-10-22]
----------------------------

Bug Fixes

* The argument 'browser' introduced in version 0.3.0 has been removed
  again. The argument was set by default to the output of
  getOptions('browser'), if interactive() returned TRUE, otherwise to
  'false'. The function getOptions('browser') returns either a string
  or a function call. The later caused an error message, as
  experienced with RStudio and RGui.exe. The check is now handled
  internally by plot.gvis.

  Thanks to Sebastian Kranz for reporting this bug.


googleVis 0.3.0 [2012-10-20]
----------------------------

NEW FEATURES

* plot.gvis has a new argument 'browser'. The argument is passed on
  to the function browseURL. The 'browser' argument is by default set
  based on the output of interactive(). This prevents R CMD CHECK
  trying to open browser windows during the package checking
  process. See the help file of plot.gvis for more details.
  Thanks to Henrik Bengtsson for his comments and suggestions.

* gvisMotionChart has new arguments xvar, yvar, colorvar and
  sizevar. Those arguments are optional and set the various dimensions 
  of a motion chart, similar to those in gvisBubbleChart.
  Thanks to Sebastian Kranz for the idea and initial code.

* gvisGeoChart accepts tooltip.triggers following an update of the
  Visualisation API by Google, 24 September 2012

* R data frames are transformed into JSON objects using a new function 
  provided by Sebastian Kranz and Wei Luo. The new function speeds up 
  the googleVis functions.

Changes

* Changed the load mechanism for the Google API from http to https.
  Thanks to Erik Bülow for pointing this out (Issue 19). 

* Changed example in help file of gvisMap to show how to include html
  code in tooltip. 

Bug Fixes

* Chart editor was not validated properly under XHMTL 1.0 Strict


googleVis 0.2.17 [2012-08-02]
----------------------------

Changes

 * Added sections with information to 'knitr' and 'Rook' to vignette 

 * Added example to gvisMerge demonstrating the use of 'Reduce'

Bug Fixes

 * Data frames with one row only were not displayed in a chart.
   Thanks to Oliver Jay and Wai Tung Ho for reporting this issue.

 * Fixed earth quake example, using data from 
   http://www.iris.edu/seismon/last30.html, 
   Mag was read as factor rather than numeric

googleVis 0.2.16 [2012-06-01]
----------------------------

Changes

 * Updated example in help file of gvisGeoChart for individual colour
   axis 

 * Updated links to Google API pages

NEW FEATURES

 * gvisMotionCharts accepts quarterly and weekly time dimensions.
   Thanks to Jason Pickering for providing a patch. 

googleVis 0.2.15 [2012-03-04]
----------------------------

Changes

*  Updated documentation following a new version of the Google API
   on 22 February 2012. 
     
*  Moved vignette from folder /inst/doc to /vignettes

NEW FEATURES

*  Quoted from Google
   http://code.google.com/apis/chart/interactive/docs/release_notes.html: 
   - Added gradient color mode to bubble chart.
   - Geo chart:
     o  Region interactivity in marker mode is now disabled by
     	default. How to keep the old behavior? Set the
   	enableRegionInteractivity option to true.

     o  Markers are now opaque by default. How to keep the old
        behaviour? Set the markerOpacity option to 0.5.

     o  Marker size is now between 3 and 12 pixels by default. How to
        keep the old behavior? Set the sizeAxis option to {minSize: 2,
        maxSize: 30}.

     o  A magnifying glass is now opened when the user hovers over
        cluttered markers (excluding IE<=8). How to keep the old
        behaviour? Set the magnifyingGlass option to {enable: false}.

     o  Maps are not stretched by default anymore, but rather kept at
      	the original aspect ratio. How to keep the old behavior? Set the
  	keepAspectRatio option to false.


googleVis 0.2.14 [2012-02-04]
----------------------------

Changes

*  Updated help files to be in line with the Google Visualisation
   API pages
*  Updated vignette with new section on dealing with apostrophes in
   column names and updated example in section "Setting options"
*  Fixed typos in vignette. Thanks to Pat Burns for pointing them
   out
*  Updated links to Google's updated API Terms of Use:
   http://code.google.com/apis/terms/index.html  

NEW FEATURES

 *  New bubble chart function gvisBubbleChart


googleVis 0.2.13 [2011-12-19]
----------------------------

Changes

 *  The list of arguments for gvisGeoChart changed:
    - the argument 'numvar' has been renamed to 'colorvar' to
      reflect the updated Google API. Additionally gvisGeoChart
      gained a new argument 'sizevar'.
 *  Updated googleVis vignette with a section on using googleVis 
    output in presentations  
 *  Renamed demo EventListner to EventListener

NEW FEATURES

 *  Google published a new version of their Visualisation API on 7
    December 2011. Some of the new features have been implemented
    into googleVis already:
    - New stepped area chart function gvisSteppedAreaChart
    - gvisGeoChart has a new marker mode, similar to the mode in
      gvisGeoMap. See example(gvisGeoChart) for the new
      functionalities.

googleVis 0.2.12 [2011-12-07]
----------------------------

Bug Fixes

 *  gvisMotionChart didn't display data with special characters,
    e.g. spaces, &, %, in column names correctly. 
    Thanks to Alexander Holcroft for reporting this issue.

googleVis 0.2.11 [2011-11-16]
----------------------------

Changes

*  Updated vignette and documentation with instructions on changing
   the Flash security settings to display Flash charts locally. 
   Thanks to Tony Breyal.
*  New example to plot weekly data with gvisMotionChart
*  Removed local copies of gadget files to reduce package file
   size. A local copy of the R script to generate the original gadget
   files is still included in inst/gadgets 

googleVis 0.2.10 [2011-09-24]
----------------------------

Changes

*  Updated section 'Using googleVis output with Google Sites,
   Blogger, etc.' vignette

*  Updated example for gvisMotionChart, showing how the initial
   chart setting can be changed, e.g to display a line chart.

*  New example for gvisAnnotatedTimeLine, showing how to shade
   areas. Thanks to Mike Silberbauer for providing the initial code.    
   
NEW FEATURES
 
 *  New demo WorldBank. It demonstrates how country level data can
    be accessed from the World Bank via their API and displayed with a
    Motion Chart. Inspired by Google's Public Data Explorer, see
    http://www.google.com/publicdata/home
  

googleVis 0.2.9 [2011-09-01]
---------------------------

Changes

*  The documentation of googleVis has been update to reflect a new
   version of the Google Visualisation API which was published on 
   13 July, see
   http://code.google.com/apis/chart/interactive/docs/release_notes.html#72011. 
   Here are some of the most interesting features:   
   - Support for dual Y axes
   - Ability to crop and zoom chart area to specific ranges
   - Ability to set different properties for each series
   - Ability to enable or disable chart interactivity
   - Performance improvements in GeoChart

*  Updated vignette with new sections on
   - Setting options
   - How to use the on-page chart editor
   - Using googleVis with other Google products such as
     Blogger and Google Sites 

*  Updated warning section for gvisTreeMap

NEW FEATURES
 
 *  New gvis.editor argument in options, which adds an edit
    button to the page, allowing the user to edit, change and
    customise the chart on the fly.


googleVis 0.2.8 [2011-07-31]
---------------------------

Changes

*  Updated package welcome message. The message asks the user to read Google's
   Visualisation and Maps API Terms of Use before she uses the functions of the
   googleVis package. 
	
*  The caption gvis-plots contain an additional link to Google's data policy.

*  New example for gvisBarChart using the XML package to chart online data from Wikipedia


googleVis 0.2.7 [2011-07-10]
---------------------------

Changes

*  The vignette includes new sections describing:
   - how output of the googleVis package can be included into
     WordPress pages,  
   - how JavaScript event handlers can be added to charts. 

*  Clarified documentation for Flash based charts in help files of 
   motion chart, geo map, annotated time line. 

NEW FEATURES
 
 *  New demo 'EventListener' showcasing how a 'Listener' event can be
    added to charts  

BUG FIXES

 *  gvisGeoMap documentation stated that the default dataMode is
    'regions', but the function actually used 'markers'. The default
    for dataMode is now 'regions' and therefore in line with the
    help file.   

googleVis 0.2.6 [2011-06-12]
---------------------------

Changes

*  Updated demos

NEW FEATURES

*  New interfaces to three more interactive Google charts:
   - gvisComboChart
   - gvisGeoChart
   - gvisCandlestickChart

*  New function 'gvisMerge' to align two charts next to each other


googleVis 0.2.5 [2011-06-04]
---------------------------

NEW FEATURES

*  New interfaces to more interactive Google charts:
   - gvisLineChart
   - gvisBarChart
   - gvisColumnChart
   - gvisAreaChart
   - gvisScatterChart
   - gvisPieChart
   - gvisGauge
   - gvisOrgChart
   - gvisIntensityMap 

*  New demo 'AnimatedGeoMap'. The demo shows how a Geo Map can be animated
   with additional JavaScript. 
   Thanks to Manoj Ananthapadmanabhan and Anand Ramalingam, who
   provided the idea and initial code.
    
BUG FIXES

*  The way RJSONIO treats backslashes changed in version 0.7.1 and
   as a result some Google charts were no longer displayed.

googleVis 0.2.4 [2011-02-07]
---------------------------

Changes
   
*  plot.gvis no longer writes into the package folder. Instead
   temporary files are created. This overcomes the need to install
   the package into a directory with write access. Many thanks to
   Ben Bolker for this suggestion and code contribution.  
  
*  plot.gvis no longer requires the web server provided by
   the R.rsp package to display the visualisation output. Instead it
   uses the internal R HTTP help server. Many thanks to John Verzani
   for this suggestion and code contribution. 
  
*  R >= 2.11.0 is required to plot googleVis output, as it uses the
   internal R HTTP help server.
  
*  Updated vignette with a section on how to use googleVis with
   RApache and brew

NEW FEATURES

*  The plot function generates a web page which includes a link
   to the HTML code of the chart. Many thanks to Henrik Bengtsson
   for this suggestion.

*  gvis visualisation functions have a new argument 'chart id', to
   set the chart id of the exhibit manually. 	         

*  gvis functions return more details about the visualisation chart
   in a structured way. Suppose x is a 'gvis' object, than
   x$html$chart is a named character vector of the chart's
   JavaScript building blocks and html tags. 

*  print.gvis has a new argument 'tag', which gives the user more
   control over the output

*  Brew example files in: 
   system.file("brew", package = "googleVis")  

BUG FIXES

*  gvisTable did not accept datetime columns.

googleVis 0.2.3 [2010-12-19]
---------------------------

Changes
    
NEW FEATURES

*  gvisAnnotatedTimeLine accepts date in POSIX* formats

BUG FIXES

*  Google date objects expect the months Jan.- Dec. as 0 - 11 and
   not 1 - 12 
*  Fixed typo in the Andrew data set. The Pressure at 1992-08-24
   12:00:00 was 951 and not 51  

googleVis 0.2.2 [2010-12-12]
---------------------------

Changes
    
 *  Fixed typos in documentation

NEW FEATURES

*  New function:
   - createGoogleGadget which allows users to create Google Gadgets
     XML output  


googleVis 0.2.1 [2010-11-30]
---------------------------

Changes
    
 *  First version to be released on CRAN

NEW FEATURES

*  New function:
   - gvisAnnotatedTimeLine to generate interactive annotated time
     line charts 

googleVis 0.2.0 [2010-11-14]
---------------------------

Changes

*  The package has been renamed from GoogleMotionChart to googleVis 
   to reflect a new more flexible implementation.
*  More functions of the Google Visualisation API are now available.

USER-VISIBLE CHANGES

*  New interfaces, all visualisation functions start with 'gvis'.
*  Output is now of class 'gvis' with generic print and plot
   functions.
*  'gvis' objects are list of lists, which allow the user to extract
   the various parts of the visualisation output, e.g. the chart
   object.
  
NEW FEATURES

*  New functions:
   - gvisMotionChart to generate motion charts
   - gvisGeoMap to generate geographical maps
   - gvisMap to generate maps
   - gvisTreeMap to generate tree maps
   - gvisTable to generate table output
   - print.gvis: generic function to print 'gvis' objects
   - plot.gvis: generic function to display 'gvis' objects in a
     browser via the R.rsp package.  


googleVis 0.1.4 [2010-08-12]
---------------------------
Changes

*  The package uses the RJSONIO package from Omegahat to
   transform a data.frame into a json DataTable 

googleVis 0.1.3 [2010-08-08]
---------------------------
NEW FEATURES

*  More detailed motion chart configuration settings are possible.

USER-VISIBLE CHANGES
*  options have to be set via a list. Arguments height and width
   can be set, plus further configurations.
*  Updated demo PerformanceAnalyticsMotionChart   


googleVis 0.1.2 [2010-08-03]
---------------------------

First public version.
```