# Highlights from the Shiny Developer Conference

Website: http://www.rstudio.com/shinydevcon  
Twitter: [#shinydevcon](http://twitter.com/hashtag/shinydevcon)

## Reactivity tutorial

Joe Cheng explaining the philosophy behind Shiny’s reactive programming framework and exploring patterns and techniques for using it well.

- Prefer using reactive expressions to model calculations, over using observers to set (reactive) variables.
- `reactive()` is for calculating values, without side effects.
- `observe()` is for performing actions, with side effects.

| `reactive()` | `observe()` |
| ---------- | --------- |
| Callable   | 	Not callable |
| Returns a value | No return value |
| Lazy |	Eager |
| Cached | N/A |

Code on GitHub: https://github.com/rstudio/reactivity-tutorial (see branch `with-solutions` for answers)

## Shiny Gadgets 

*Things that are hard to express with code but you want to do reproducibly* -- Hadley Wickham

Build interactive graphical tools for exploratory data analysis that run locally, taking your data as input and returning a result. [Read more](http://shiny.rstudio.com/articles/gadgets.html)

## Debugging Shiny applications

Debugging
- breakpoints using RStudio
- conditional breakpoints with `browser()`

Tracing
- showcase mode: `runApp(..., display.mode = "showcase")`
- reactive log: `options(shiny.reactlog = TRUE)`, start visualization in app by hitting `Ctrl+F3`
- `cat`
- shinyapps.io: `rsconnect::showLogs(streaming = TRUE)`
- Shiny Server: `tail -f /var/log/shiny-server/myapp-20160131-104403-8492.log`
- client/server: `options(shiny.trace = TRUE)`

Error handling
- stack traces
- pause on errors: `options(shiny.error = browser)`
- JavaScript dev mode on OS X: `defaults write org.rstudio.RStudio WebKitDeveloperExtras -bool true`

[Slides](http://rpubs.com/jmcphers/149638) &bull; [Article](http://shiny.rstudio.com/articles/debugging.html)

## Further reading

- [Shiny Developer Conference 2016 Recap](http://www.r-bloggers.com/shiny-developer-conference-2016-recap/) by VP Nagraj
- [Shiny Developers Conference Review](http://www.r-bloggers.com/shiny-developers-conference-review/) by Aimee Gott
- [Shiny Developer Conference](http://www.r-bloggers.com/shiny-developer-conference/) by John Mount
- [DataScienceLA](http://www.youtube.com/user/DataScienceLA) interviews with by Joe Cheng, Yihui Xie, Hadley Wickham and JJ Alaire
