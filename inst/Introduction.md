

# REPLesentR: Presentations inside the R REPL

author: Sebastian Warnholz  
date: 2018-10-30  
email: wahani@gmail.com  



# Features

- Tools to do presentations inside the R REPL
- Take advantage of RMarkdown and pandoc
- Evaluate code on slides
- Integrate data visualisations using the fantastic 'txtplot' package

//empty

- Wish-list:
    - Syntax highlighting on slides
    - Colours on slides
    - Satisfying set of formats for slides
    - Number of slide in lower right corner



# Commands in Presentation Mode

-   n -- next slide
-   p -- previous slide
-   f -- first slide
-   l -- last slide
-   e -- evaluate code
-  ee -- evaluate code until here
-  cc -- recompile slide deck
-   q -- quit presentation
-   h -- show this help



# Evaluation of code

Try this now by typing 'e'

//code

```r
hi <- "Hi\n"
cat(hi)
```

# Slide formats

- `//center`
    - needs to be at the beginning of a line
    - in the title it defines the slide layout
- `//code`
    - put this right in front of a code block
    - will make this code block available for evaluation
- `//empty`
    - for empty lines


# Slide formats examples

//center type 'e' to see the source of this slide

//empty

//code

```r
.fileName <- system.file("Introduction.Rmd", package = "REPLesentR")
.allSlide <- readLines(.fileName)
.thisSlidePosition <- grep("^# slide formats examples", .allSlide, TRUE)
.thisSlide <- .allSlide[.thisSlidePosition:(.thisSlidePosition + 14)]
for (row in .thisSlide) cat(row, "\n")
```

# //center Make great plots with 'txtplot'!


```
    +-----+-----------+----------+-----------+-----------+-+
    |                                               *   *  |
 10 +                                                 *    +
    |                                        *             |
  5 +                                     *  *             +
    |                                 *     *              |
    |                           *  *                       |
  0 +                  *     * *  **                       +
    |               *                                      |
 -5 +                *                                     +
    |                                                      |
    |                                                      |
-10 + *                                                    +
    +-----+-----------+----------+-----------+-----------+-+
         -2          -1          0           1           2  
```

# Start from an example

You can find the source of this presentation by typing 'e':

//code

```r
print(system.file("Introduction.Rmd", package = "REPLesentR"))
```


# //center Inspiration for this package comes from:

//center https://github.com/marconilanna/REPLesent


# //center THE END!
