---
title: 'Test Chapter 1'
description: 'Messing around with differing ways to ask questions'
---

## Variable names and means

```yaml
type: NormalExercise
key: e7dd2640c5
xp: 100
```

In this course, if you learn anything, I would be quite impressed, as it has been designed for me to learn the basics of DataCamp

`@instructions`
Create a variable named "x" that is a vector containing the three numbers: 2,3, and 7. Then, set a variable called "mean.x" to be the mean of this vector.

`@hint`
Assign a group of numbers  to a variable using c(…)
The "mean()" function is useful for finding the mean of a vector

`@pre_exercise_code`
```{r}
rm(list=ls())
```

`@sample_code`
```{r}
#Define Variable x
x=___
x

#Define the mean of x
mean.x=___
mean.x
```

`@solution`
```{r}
#Define Variable x
x=c(2,3,7)
x

#Define the mean of x
mean.x=mean(x)
mean.x
```

`@sct`
```{r}
ex() %>% check_object("x") %>% check_equal()
ex() %>% check_object("mean.x") %>% check_equal()
success_msg("Well Done!")
```

---

## some simple data frames

```yaml
type: NormalExercise
key: f3cc5f9d8c
xp: 100
```

Now to try doing things with data frames and what not

`@instructions`
Access the Data frame "mtcars" and create a vector named "means" that holds the means for "mpg","hp",and "qsec"

`@hint`
df[row,col] can be used to access a data frame named df with specified rows and columns

`@pre_exercise_code`
```{r}
rm(list=ls())
```

`@sample_code`
```{r}
#find the mean of mpg
mean.mpg=___
mean.mpg

#find the mean of hp
mean.hp=___
mean.hp

#find the mean of qsec
mean.qsec=___
mean.qsec

#combine the means
means=___
```

`@solution`
```{r}
mean.mpg=mean(mtcars$mpg)
mean.hp=mean(mtcars$hp)
mean.qsec=mean(mtcars$qsec)
means=c(mean.mpg,mean.hp,mean.qsec)
```

`@sct`
```{r}
ex() %>% check_object("means") %>% check_equal()
success_msg("Well Done! You have combined named vectors into 1 bigger vector")
```

---

## remake fitting Galtons Height data

```yaml
type: NormalExercise
key: 069b2bedc8
xp: 100
```

The Galton data has already been read into a dataset called 
`heights`. These data include the heights of 928 adult children `child_ht`, together with an index of their parents' height `parent_ht`. The video explored the distribution of the parents' height; in this assignment, we investigate the distribution of the heights of the adult children.

`@instructions`
- Define the height of an adult child as a local variable

- Use the function [mean()](https://www.rdocumentation.org/packages/base/versions/3.5.0/topics/mean/) to calculate the mean and the function [sd()](https://www.rdocumentation.org/packages/base/versions/3.5.0/topics/sd/) to calculate the standard deviation

-Use the normal approximation and the function [pnorm()](https://www.rdocumentation.org/packages/stats/versions/3.5.0/topics/Normal/) to determine the probability that a child's height is less than 72 inches.

`@hint`
Remember that we can reference a variable, say `var`, from a data set such as `heights`, as `heights$var`.

`@pre_exercise_code`
```{r}
rm(list=ls())
heights <- read.csv("https://assets.datacamp.com/production/repositories/2610/datasets/c85ede6c205d22049e766bd08956b225c576255b/galton_height.csv", header = TRUE)
```

`@sample_code`
```{r}
#Define the variable
ht_child <- ___

#Calculate the mean height
mchild <- ___
mchild

#Calculate the standard deviation of heights
sdchild <- ___
sdchild

#Determine the probability that a child's height is less than 72 inches
pr=___(___, mean=___, sd=___)
pr
```

`@solution`
```{r}
ht_child <- heights$child_ht
mchild <- mean(ht_child)
sdchild <- sd(ht_child)
pr=pnorm(72,mean=mchild, sd=sdchild)
```

`@sct`
```{r}
ex() %>% check_object("pr") %>% check_equal()
success_msg("Well Done! You did the thing")
```

---

## maybe get graphical?

```yaml
type: NormalExercise
key: a984d75d4e
xp: 100
```

lets see if graphing is a thing

`@instructions`
use [lm()] to graph mpg vs hp in the mtcars dataframe

`@hint`
You can use the "lm" function in order to create a linear regression model that attempts to explain y based on x (Y~X)

`@pre_exercise_code`
```{r}
rm(list=ls())
```

`@sample_code`
```{r}
#plot Miles per gallon against Horsepower
plot(x=___,y=___,pch=19,xlab="Miles per Gallon",ylab="Horsepower",main="Miles per Gallon vs Horsepower")
legend("topright",legend="Regression Line",lty=3,col="red")

#create a linear model
MPG.vs.HP=___(___~___,data=___)

#add the model to the graph
abline(___,lty=3,col="red")

```

`@solution`
```{r}
plot(x=mtcars$mpg,y=mtcars$hp,pch=19,xlab="Miles per Gallon",ylab="Horsepower",main="Miles per Gallon vs Horsepower")
legend("topright",legend="Regression Line",lty=3,col="red")
MPG.vs.HP=lm(hp~mpg,data=mtcars)
abline(MPG.vs.HP,lty=3,col="red")
```

`@sct`
```{r}
ex() %>% check_object("MPG.vs.HP") %>% check_equal()
success_msg("Wow! graphing does work well in this")
```

---

## Pure Mult choice testing?

```yaml
type: PureMultipleChoiceExercise
key: e7cc439bbe
xp: 50
```

Which of the following is the correct answer if 2 is the correct answer

`@hint`
is it option 2 or the number 2, who will ever know?

`@possible_answers`
- 1
- [it might possibly be this one...]
- 2
- 4

`@feedbacks`
- 1 is not correct...
- You got it!
- its not this two...
- and 4 is forever

---

## Console'd mult choice

```yaml
type: MultipleChoiceExercise
key: bc5e7d4e7b
xp: 50
```

Just try and figure out which one of these pointless answers is the right answer. 
- I am truthfully just testing out the MC with the console!

`@possible_answers`
- Not this one
- Its this one
- sqrt(24)
- [The Spanish inquisition]

`@hint`
Its labeled...

`@pre_exercise_code`
```{r}
rm(list=ls())
```

`@sct`
```{r}
msg1 = "Incorrect ya goob"
msg2 = "Never trust me"
msg3 = "it wasnt rational to pick this"
msg4 = "Nobody expects the spanish inquisition..."
 ex() %>% check_mc(4, feedback_msgs = c(msg1, msg2, msg3, msg4))
```

---

## Iterative testing

```yaml
type: BulletExercise
key: 53cda0b8d5
xp: 100
```

lets try combining things using `c(…)`

`@pre_exercise_code`
```{r}
rm(list=ls())
```

***

```yaml
type: NormalExercise
key: b865ae6da5
xp: 20
```

`@instructions`
combine the numbers 3,5,7 into a vector named x

`@hint`
use x=c(___) to fill it in

`@sample_code`
```{r}
x=
x
```

`@solution`
```{r}
x=c(3,5,7)
x
```

`@sct`
```{r}
ex() %>% check_object("x") %>% check_equal()
success_msg("You did it!!")
```

***

```yaml
type: NormalExercise
key: bd4bc45afa
xp: 20
```

`@instructions`
combine the numbers 10,14, and sqrt(14) into a vector named y

`@hint`
you can run operators inside of c(…)
make sure all "(" have a matching ")".

`@sample_code`
```{r}
y=
y
```

`@solution`
```{r}
y=c(10,14,sqrt(14))
y
```

`@sct`
```{r}
ex() %>% check_object("y") %>% check_equal ()
success_msg("You did it again!")
```

***

```yaml
type: NormalExercise
key: d346bfe0f8
xp: 20
```

`@instructions`
create a vector `mean.mtcars` that is just the mean of mpg in mt.cars

`@hint`
make sure to use $ to specify which column of the dataframe you want to reference. type mtcars to see the entirety of mtcars, or head(mtcars) for the first 6 rows

`@sample_code`
```{r}
mean.mtcars=
mean.mtcars
```

`@solution`
```{r}
mean.mtcars=mean(mtcars$mpg)
mean.mtcars
```

`@sct`
```{r}
ex() %>% check_object("mean.mtcars") %>% check_equal()
success_msg("wow you're getting good at this!")
```

***

```yaml
type: NormalExercise
key: 2282c7df4e
xp: 20
```

`@instructions`
now see what happens when you combine all of the vectors you have made! put x,y, and mean.mtcars into a vector, `v`.

`@hint`
you can still use c(…) to combine vectors!

`@sample_code`
```{r}
v=
v
```

`@solution`
```{r}
v=c(x,y,mean.mtcars)
v
```

`@sct`
```{r}
ex() %>% check_object("v") %>% check_equal()
success_msg(You have mastered using c(...))
```

***

```yaml
type: NormalExercise
key: 60a02eac4f
xp: 20
```

`@instructions`


`@hint`


`@sample_code`
```{r}

```

`@solution`
```{r}

```

`@sct`
```{r}

```
