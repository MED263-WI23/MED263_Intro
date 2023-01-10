# Tutorial: Installing R and Rstudio

## Background on R and Rstudio

<img height="80" alt="image" src="https://www.r-project.org/logo/Rlogo.png">

## R
#### What is R?
R is an open source, free software language popular among data scientists and bioinformaticians. Its focus is on statistics and graphics.
"Under the hood", R is written in C and Fortran, but R itself is an interpreted language, meaning that there is no need to pre-compile. R will interpret and run your code in one step.

#### Why use R
- Lots of great packages. If you're trying to do something, chances are there's a package for that
- Simple syntax and helpful error messages make coding relatively easy
- Rstudio is great
- Pretty pictures (compared to python)
- Almost all of the speakers in this class are doing something in R

<img height="80" alt="image" src="https://www.rstudio.com/wp-content/uploads/2018/10/RStudio-Logo-Flat.png">

#### What is Rstudio?
Rstudio is an Integrated Development Environment (IDE) designed for writing and testing R code. 

#### Why use Rstudio?
- Plots, variables, etc. can be easily viewed (helps with debugging)
- Easy to run specific lines or chunks of code (Command+Enter on mac, Ctrl+Enter on windows)
- Easy to search package and function documentation even when offline
- Helps with git and package development

### Install R
The newest version of R is: R 4.2.2 "Innocent and Trusting" released on 2022/10/31
They always have weird names...
CRAN is your source for (almost) everything R: (https://cran.r-project.org/)
Here, we want to install a binary. This means that we just want the compiled version that runs on our operating system (OS). Sometimes, we will want to download all the code that is used to write a language/package and then compile it ourselves.

Because each OS is different, you need to download the binary which is specific to your OS:
- Linux: (https://cran.r-project.org/bin/linux/)
- Windows: (https://cran.r-project.org/bin/windows/)
- Mac: (https://cran.r-project.org/bin/macosx/)
#### Macs be careful. M1 and newer macs download the top binary (R-4.2.2-arm64.pkg). Older intel macs download the one below (R-4.2.2.pkg).

To test if we've installed R, open a terminal and execute:
```bash
R
```
which should start R within your terminal

To see where packages will be installed, run:
```R
.libPaths()
``` 
in R. 
Most of the time, this will also tell you where your version of R is installed. Just change 'library' to 'bin/R'

Run :
```R
q()
``` 
to exit R and go back to your terminal

Working in a terminal-like application would be pretty annoying, so we want Rstudio to make it as easy as possible.

### Install Rstudio

Install Rstudio by downloading from here: (https://posit.co/download/rstudio-desktop/)
Note that we just did step 1, so we can skip that. Again, make sure you download the right one for your Operating System.

## Intro to R

### Basic Commands
1. Printing
```R
x <- 'Hello World'
print(x)
```
Should print the following
```R
'Hello World'
```

2. Comments
 ```R
#This is a single line comment
```

3. Create a vector using ```c()``` and check its length
```R
vec <- c(0, 1, 2, 3, 4, 5, 6)
print(length(vec))
```

4. Basic For Loops  
 ```R
sample_vec <- c(1, 3, 5, 7)

# Here, x will take on the value of the element of sample_vec
for (x in sample_vec){
    print(x)
}
```
Should print the following:
 ```R
> 1
> 3
> 5
> 7
```

5. Basic While Loop
 ```R
i <- 1
while (i < 5) {
    i <- i + 1
}
print(i)
```
Should print the following:
 ```R
> 5
```

6. Install a package (do this once)

If available on CRAN, we can install with the ```install.packages()``` function

 ```R
 install.packages("ggplot2")
```

7. Load an installed package (do every R session in which you use the function)
```R
library(ggplot2)
```

8. Use seq to generate a vector
```R
?seq # Will show you the documentation for the seq() function
x_vec <- seq(from = -10, to = 10, by = .1)
print(x_vec)

# We can also generate a vector in increments of 1 using c()
other_vec <- c(1:10)
print(other_vec)
```

9. Write a function that takes input x and returns the square of the sine of x
```R
sine_squared <- function(x){
   return(sin(x)*sin(x))
}
```

10. Use sapply to apply a function to a vector
```R
?sapply # Bring up the documentation for the sapply() function
y_vec <- sapply(X = x_vec, FUN = sine_squared)

# Note that this is equivalent to:
?rep
# Fill y_vec1 with zeroes first
y_vec1 <- rep(x = 0, length.out = length(x_vec))
for (i in c(1:length(x_vec)){
   y_vec1[i] <- sine_squared(x_vec[i])
}

# Check that they're the same
y_vec == y_vec1
```

11. Create a data.frame
```R
?data.frame # Bring up the documentation for the data.frame() function
df <- data.frame("x_data" = x_vec, "y_data" = y_vec)
print(df)
```

11. Plot the sine square function using ggplot
```R
plot1 <- ggplot(data = df) + geom_line(aes(x = x_data, y = y_data), color = "red", linewidth = 2) 
print(plot1)

# Add the individual data points using ggplot's geom_point
print(plot1 + geom_point(data = df, aes(x = x_data, y = y_data), color = "black", size = 1))
```

## Bonus: Changing R versions
I recently wanted to upgrade R. Unfortunately, this meant I would lose the packages I installed and would have to re-install all of them :(   The following lines help by installing all the my old packages in the new R, so long as they're available from CRAN or Bioconductor. Note: install the new R before doing this, then do this in the new R. The new R version will automatically become the default in Rstudio.

```R
# Get library locations
print(.libPaths())


# Manually set to old version (which has all your packages)
lib_loc <- "/Library/Frameworks/R.framework/Versions/4.1/Resources/library"
to_install <- unname(installed.packages(lib.loc = lib_loc)[, "Package"])
print(to_install)

# First, install from CRAN
install.packages(pkgs = to_install)

# Then, get those that aren't CRAN
tmp <- installed.packages()
installedpkgs <- as.vector(tmp[is.na(tmp[,"Priority"]), 1])
missing_from_cran <- setdiff(to_install, installedpkgs)

# Install the non-CRAN first using Bioconductor
BiocManager::install(missing_from_cran)
```

## Helpful Links:
### [Installing R + Rstudio](https://rstudio-education.github.io/hopr/starting.html)
### [Updating R (mac)](https://github.com/AndreaCirilloAC/updateR)
### [Updating R (windows)](https://talgalili.github.io/installr/)
### [base-r-cheatsheet.pdf](https://www.i3s.unice.fr/~malapert/R/pdf/base-r.pdf)

