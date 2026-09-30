# Practical 1: Basics of R Programming

a <- 10
b <- 5

# Data Types
num <- 100
char <- "MSc"
logical <- TRUE

# Operators
sum <- a + b
sub <- a - b
mul <- a * b
div <- a / b

print(sum)
print(sub)
print(mul)
print(div)

# Practical 2: Implement R Loops

## For Loop


for(i in 1:5)
{
    print(i)
}


## While Loop

```r
j <- 1

while(j <= 5)
{
    print(j)
    j <- j + 1
}
```

---

# Practical 3: Functions in R

## Example 1: Add Two Numbers

```r
add <- function(a, b)
{
    result <- a + b
    return(result)
}

sum <- add(10, 20)
print(sum)
```

## Example 2: Find Square of a Number

```r
square <- function(x)
{
    return(x^2)
}

print(square(5))
```

## Example 3: Function Without Arguments

```r
greet <- function()
{
    print("Welcome to R Programming")
}

greet()
```

## Example 4: Find Maximum of Two Numbers

```r
maximum <- function(a, b)
{
    if(a > b)
        return(a)
    else
        return(b)
}

print(maximum(15, 10))
```

---

# Practical 4: Data Frames and Probability Distribution

## A) Data Frames using cbind() and rbind()

```r
marks <- data.frame(
    Marks = c(85, 90, 99)
)

print(marks)

# Combine Columns
result <- cbind(student, marks)
print(result)
```

### Joining Rows Using rbind()

```r
# Data Frame 1
df1 <- data.frame(
    RollNo = c(1, 2),
    Name = c("Saloni", "Kartik")
)

# Data Frame 2
df2 <- data.frame(
    RollNo = c(3, 4),
    Name = c("Vipul", "Sahil")
)

# Combine Rows
new_df <- rbind(df1, df2)
print(new_df)
```

## B) Probability Distributions

### Normal Distribution

```r
print(dnorm(65, mean = 60, sd = 5))
print(pnorm(65, mean = 60, sd = 5))
print(qnorm(0.96, mean = 60, sd = 5))

set.seed(100)
print(rnorm(5, mean = 60, sd = 5))
```

### Poisson Distribution

```r
print(dpois(7, lambda = 8))
print(ppois(7, lambda = 8))
print(qpois(0.95, lambda = 8))

set.seed(100)
print(rpois(5, lambda = 8))
```

### Uniform Distribution

```r
print(dunif(64, min = 1, max = 100))
print(punif(64, min = 1, max = 100))
print(qunif(0.95, min = 1, max = 100))

set.seed(100)
print(runif(6, min = 1, max = 100))
```

### Exponential Distribution

```r
print(dexp(1, rate = 2))
print(pexp(1, rate = 2))
print(qexp(0.95, rate = 2))

set.seed(100)
print(rexp(1, rate = 2))
```

---

# Practical 5: String Manipulation in R

```r
# Creating a string variable
str <- "R Programming Language"

print(nchar(str))
print(toupper(str))
print(tolower(str))
print(strrep("R", 5))
print(sub("Programming", "Coding", str))
print(strsplit(str, " "))
print(identical("R", "R"))
print(trimws(" R Programming  "))
```

---

# Practical 6: Data Structures in R

## Vector

Stores elements of the same data type.

```r
vector_data <- c(10, 20, 30, 40, 50)

print(vector_data)
```

## List

Stores elements of different data types.

```r
list_data <- list(
    Name = "Rahul",
    Age = 22,
    Percentage = 85.5,
    Passed = TRUE
)

print(list_data)
```

## Data Frame

Stores data in rows and columns.

```r
student_data <- data.frame(
    RollNo = c(1, 2, 3),
    Name = c("Saloni", "Sayali", "Kartik"),
    Marks = c(57, 78, 98)
)

print(student_data)
```

## Accessing Elements

```r
# Accessing second element of vector
print(vector_data[2])

# Accessing Name from list
print(list_data$Name)

# Accessing Marks from data frame
print(student_data$Marks)
```

---

# Practical 7: Read and Analyze a CSV File in R

```r
getwd()

data <- read.csv("prac7.csv")

data
head(data)
tail(data)
str(data)
summary(data)
dim(data)
names(data)

print(data[, 1])

mean(data$marks)
```

---

# Practical 8: Create Different Graphs using R

## Pie Chart

```r
students <- c(40, 30, 20, 10)

dept <- c("Science", "Commerce", "Arts", "Management")

pie(
    students,
    labels = dept,
    main = "Student Distribution by Department"
)
```

## Bar Chart

```r
barplot(
    students,
    names.arg = dept,
    main = "Student Distribution by Department",
    xlab = "Departments",
    ylab = "Number of Students",
    col = "lightblue"
)
```

## Histogram

```r
sales <- c(40, 50, 60, 70, 80, 90)

hist(
    sales,
    col = "cyan",
    main = "Histogram",
    xlab = "Marks"
)
```

## Scatter Plot

```r
n <- as.integer(
    readline(prompt = "Enter the number of data points:")
)

x <- numeric(n)
y <- numeric(n)

for(i in 1:n)
{
    x[i] <- as.numeric(
        readline(prompt = paste("Enter X", i, ":"))
    )

    y[i] <- as.numeric(
        readline(prompt = paste("Enter Y", i, ":"))
    )
}

print(x)
print(y)

plot(
    x,
    y,
    main = "Scatter Plot",
    xlab = "X",
    ylab = "Y",
    pch = 19,
    col = "blue"
)
```

---

# Practical 9: Statistical Analysis in Excel

Create a dataset and perform statistical analysis using Excel.

### Functions / Topics

- AVERAGE
- MAX
- MIN
- COUNTIF
- COUNTA
- Anchoring
- IF
- Nested IF
- LOWER
- CONCAT
- UPPER
- VLOOKUP
- HLOOKUP
- INDEX
- ADDRESS

---

# Practical 10: Data Analysis in Excel

## A) Data Management

- Sorting
- Filtering
- Delimiters
- Data Validation

## B) Advanced Data Analysis

- Pivot Tables
- Pivot Charts

---

# Practical 11: Advanced Data Analysis using Pivot Tables and Pivot Charts in R

```r
salesdata <- data.frame(
    dept = c(
        "Science",
        "Commerce",
        "Arts",
        "Science",
        "Commerce",
        "Arts"
    ),
    month = c(
        "Jan",
        "Jan",
        "Jan",
        "Feb",
        "Feb",
        "Feb"
    ),
    sales = c(
        5000,
        7000,
        4000,
        6000,
        8000,
        5000
    )
)

print(salesdata)

# Department-wise total sales
pivot <- stats::aggregate(
    sales ~ dept,
    data = salesdata,
    FUN = base::sum
)

print(pivot)

# Frequency table
table(salesdata$dept)

# Cross-tabulation
xtabs(
    sales ~ dept + month,
    data = salesdata
)

# Bar Plot
barplot(
    pivot$sales,
    names.arg = pivot$dept,
    main = "Department-wise Total Sales",
    xlab = "Department",
    ylab = "Total Sales",
    col = "lightblue"
)
```

---

# Practical 12: Statistical Tests in R

## T-Test

```r
group1 <- c(85, 90, 88, 92)
group2 <- c(80, 85, 75, 82, 88)

t.test(group1, group2)
```

## F-Test

```r
var.test(group1, group2)
```

## One-Way ANOVA

```r
group <- factor(
    c(
        "A", "A", "A",
        "B", "B", "B",
        "C", "C", "C"
    )
)

marks <- c(
    80, 97, 95,
    75, 67, 39,
    58, 49, 60
)

anova_result <- aov(marks ~ group)

summary(anova_result)
```

## Chi-Square Test

```r
data_matrix <- matrix(
    c(
        20, 30,
        25, 30
    ),
    nrow = 2
)

chisq.test(data_matrix)
```

## Independence of Attributes

```r
mat <- matrix(
    c(
        1, 2, 3,
        2, 4, 6,
        0, 1, 5
    ),
    nrow = 3,
    byrow = TRUE
)

q <- qr(mat)

is_independent <- q$rank == ncol(mat)

print(q$rank)
print(is_independent)
```

---


**Vaibhavi Takale**

Advanced Data Analytics – Practical Reference
