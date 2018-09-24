---
title: 'Template Chapter 1'
description: 'This is a template chapter.'
---

## An exercise title written in sentence case

```yaml
type: NormalExercise
key: 5a681e3715
lang: r
xp: 100
skills: 1
```

This is the Context. It should help provide students with the background information needed.
The Instructions that follow should be in bullet point form with clear guidance for what is expected.

`@instructions`
- Instruction 1
- Instruction 2
- Instruction 3

`@hint`
- Here is the hint for this setup problem. 
- It should get students 50% of the way to the correct answer.
- So don't provide the answer, but don't just reiterate the instructions.
- Typically one hint per instruction is a sensible amount.

`@pre_exercise_code`
```{r}
# Load datasets and packages here.
```

`@sample_code`
```{r}
# Your
# sample
# code
# should
# be
# ideally
# 10 lines or less,
# with a max
# of 16 lines.
```

`@solution`
```{r}
# Answer goes here
# Make sure to match the comments with your sample code
# to help students see the differences from solution
# to given.
```

`@sct`
```{r}
# Update this to something more informative.
success_msg("Some praise! Then reinforce a learning objective from the exercise.")
```

---

## Insert exercise title here

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

## Insert exercise title here

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

comebine the means
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

## Insert exercise title here

```yaml
type: PureMultipleChoiceExercise
key: e7cc439bbe
xp: 50
```

Which of the following is the correct answer if 2 is the correct answer

`@hint`
is it option 2 or the number 2, who will ever know?

`@possible_answers`
1. 17
2. 14
3. 2

`@feedback`
