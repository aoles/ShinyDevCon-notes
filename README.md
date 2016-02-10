# Highlights from the Shiny Developer Conference

Website: http://www.rstudio.com/shinydevcon  
Twitter: [#shinydevcon](http://twitter.com/hashtag/shinydevcon)

## Reactivity tutorial | *Joe Cheng*

Author of the Shiny reactive programming framework explains the philosophy behind reactivity and explores patterns and techniques for using it well.
- Prefer using reactive expressions to model calculations, over using observers to set (reactive) variables.
- Use reactive expressions for calculations (no side effects). Use observers for actions (side effects).

| `reactive()` | `observe()` |
| ---------- | --------- |
| Callable   | 	Not callable |
| Returns a value | No return value |
| Lazy |	Eager |
| Cached | N/A |

[Slides](https://cdn.rawgit.com/rstudio/reactivity-tutorial/master/slides.html#/warm-up-side-effects) &bull; [Tutorial](https://github.com/rstudio/reactivity-tutorial) (see `with-solutions` branch for answers)

## Interactive graphics | *Winston Chang*

- add/select single points using `click`, `dblcick`, and `hover`
- linked brushing

[Slides](https://gist.github.com/wch/25a1c4ce8fc84022d3e7)

## Shiny Gadgets | *Hadley Wickham*

*Things that are hard to express with code but you want to do reproducibly* -- Hadley Wickham

Build interactive graphical tools for exploratory data analysis that run locally, taking your data as input and returning a result.

[Article](http://shiny.rstudio.com/articles/gadgets.html)

## Modules | *Garrett Grolemund*

Manage complex Shiny apps by modularizing their code. 

[Slides](https://cdn.rawgit.com/aoles/modules-tutorial/master/01-Modules.pdf) &bull; [Tutorial](https://github.com/aoles/modules-tutorial) &bull; [Article](http://shiny.rstudio.com/articles/modules.html)

## Debugging Shiny applications | *Jonathan McPherson*

Debugging
- breakpoints using RStudio
- conditional breakpoints with `browser()`

Tracing
- showcase mode: `runApp(..., display.mode = "showcase")`
- reactive log: `options(shiny.reactlog = TRUE)`, start visualization in app by hitting `Ctrl+F3`
- print to console: `cat`
- shinyapps.io: `rsconnect::showLogs(streaming = TRUE)`
- Shiny Server: `tail -f /var/log/shiny-server/myapp-20160131-104403-8492.log`
- client/server: `options(shiny.trace = TRUE)`

Error handling
- stack traces
- pause on errors: `options(shiny.error = browser)`
- JavaScript dev mode on OS X: `defaults write org.rstudio.RStudio WebKitDeveloperExtras -bool true`

[Slides](http://rpubs.com/jmcphers/149638) &bull; [Article](http://shiny.rstudio.com/articles/debugging.html)

## HTML templates

Author the structure and style of your app's UI in HTML, but still conveniently insert input and output widgets using R functions.

[Article](http://shiny.rstudio.com/articles/templates.html)

## Building dashboards | *Nathan Stephens*

An increasingly popular use of Shiny is in building dashboards, especially since the release of the [shinydashboard](https://github.com/rstudio/shinydashboard) package.

[Project website](http://rstudio.github.io/shinydashboard/)

## Profiling | *Winston Chang*

Use [profvis](https://github.com/rstudio/profvis) to find and fix performance bottlenecks to make your apps as responsive as possible.

[Vignette](https://rpubs.com/wch/123888)

## Data Tables | *Yihui Xie*

The R package [DT](https://github.com/rstudio/DT) is an interface to the DataTables JavaScript library which renders HTML tables that can be paginated, filtered, and sorted.

## Authoring books with R Markdown  | *Yihui Xie*

Preview of the new [bookdown](http://rstudio.github.io/bookdown) package for laying out complex, multi-file documents. Features automatic numbering of figures and tables in the HTML output, cross-references of figures and tables, and fine control of the appearance of figures.

## shinyjs | *Dean Attali*

Perform common JavaScript operations in Shiny apps using plain R code
- hide an element
- disable an input
- reset an input back to its original value
- delay code execution by a few seconds
- run your own custom JavaScript functions from R
- color picker

[CRAN](http://cran.r-project.org/web/packages/shinyjs) &bull; [GitHub](http://github.com/daattali/shinyjs) &bull; [R-Podcast](https://www.r-podcast.org/posts/the-r-podcast-episode-16-interview-with-dean-attali.html) &bull; [Live demo](http://daattali.com/shiny/shinyjs-demo/)

## Radiant - Business analytics using R and Shiny | *Vincent Nijs*

[GitHub](https://github.com/vnijs/radiant) &bull; [Documentation](http://vnijs.github.io/radiant/) &bull; [R-Podcast](https://www.r-podcast.org/posts/the-r-podcast-episode-17-a-simply-radiant-chat-with-vincent-nijs.html) &bull; [Live demo](https://internal.shinyapps.io/vnijs/marketing/)

## Grid Style Sheets 2.0  | *Yihui Xie*

http://gridstylesheets.org/

## Bindings to popular JavaScript libraries | *Herman Sontrop ([Friss](http://www.friss.eu/en/))*

[GitHub](https://github.com/FrissAnalytics/shinyJsTutorials) - tutorials will appear soon

## Further reading

- [Shiny Developer Conference 2016 Recap](http://www.r-bloggers.com/shiny-developer-conference-2016-recap/) by VP Nagraj
- [Shiny Developers Conference Review](http://www.r-bloggers.com/shiny-developers-conference-review/) by Aimee Gott
- [Shiny Developer Conference](http://www.r-bloggers.com/shiny-developer-conference/) by John Mount
- [DataScienceLA](http://www.youtube.com/user/DataScienceLA) interviews with by Joe Cheng, Yihui Xie, Hadley Wickham and JJ Alaire
