# 📊 Excel for Complete Beginners — Part 2: Formulas & Functions

Now we're going to learn the part that makes Excel really powerful:

> **telling Excel how to calculate things.**

Don't worry if formulas look strange at first. We'll build them one piece at a time.

---

# 1. What Is a Formula?

A formula is an instruction that tells Excel to calculate something.

Every normal Excel formula starts with:

```text
=
```

For example:

```text
=10+20
```

Excel returns:

```text
30
```

The `=` tells Excel:

> "Don't treat what follows as ordinary text. Calculate it."

---

# 2. Basic Mathematical Operators

Excel uses these operators:

| Operation      | Symbol | Example |
| -------------- | ------ | ------- |
| Addition       | `+`    | `=10+5` |
| Subtraction    | `-`    | `=10-5` |
| Multiplication | `*`    | `=10*5` |
| Division       | `/`    | `=10/5` |
| Power          | `^`    | `=10^2` |

So:

```text
=10+5
```

gives:

**15**

```text
=10-5
```

gives:

**5**

```text
=10*5
```

gives:

**50**

```text
=10/5
```

gives:

**2**

```text
=10^2
```

gives:

**100**

---

# 3. Formulas Using Cells

This is where Excel becomes much more useful.

Suppose:

```text
A1 = 100
A2 = 50
```

In A3 write:

```text
=A1+A2
```

Result:

```text
150
```

You're telling Excel:

> Take the value in A1 and add the value in A2.

---

# 4. Why Use Cell References?

You could write:

```text
=100+50
```

But suppose the numbers change.

If A1 changes from:

```text
100
```

to:

```text
200
```

the formula:

```text
=A1+A2
```

automatically changes its result.

That's one of the fundamental ideas behind spreadsheets.

---

# 5. Multiple Operations

You can combine operations.

For example:

```text
=10+5*2
```

Excel doesn't simply calculate from left to right.

It follows mathematical order of operations.

Multiplication happens before addition.

So:

```text
10 + (5 × 2)
```

= **20**

---

# 6. Parentheses

You can control the order using parentheses.

```text
=(10+5)*2
```

First:

```text
10+5 = 15
```

Then:

```text
15*2 = 30
```

Result:

**30**

Compare:

```text
=10+5*2
```

which gives:

**20**

So parentheses matter.

---

# 7. Cell Ranges

You've already seen something like:

```text
A1:A10
```

This means:

> Every cell from A1 through A10.

Visually:

```text
A1
A2
A3
A4
A5
A6
A7
A8
A9
A10
```

This is called a **range**.

---

# 8. SUM — Your First Essential Function

Suppose:

```text
A1 = 10
A2 = 20
A3 = 30
A4 = 40
```

You could write:

```text
=A1+A2+A3+A4
```

But that's inconvenient.

Instead:

```text
=SUM(A1:A4)
```

Result:

**100**

---

# 9. Understanding Function Syntax

A function usually looks like:

```text
=FUNCTION(arguments)
```

For example:

```text
=SUM(A1:A4)
```

Here:

**SUM** = function name

**A1:A4** = argument

The parentheses contain the information the function needs.

---

# 10. SUM With Multiple Ranges

You can also provide multiple arguments.

For example:

```text
=SUM(A1:A5,C1:C5)
```

This adds both ranges.

You can also provide individual cells:

```text
=SUM(A1,A3,A7)
```

---

# 11. AVERAGE

Suppose:

```text
A1 = 70
A2 = 80
A3 = 90
```

Use:

```text
=AVERAGE(A1:A3)
```

Excel calculates:

```text
(70+80+90)/3
```

Result:

**80**

---

# 12. MIN

`MIN` finds the smallest numerical value.

```text
=MIN(A1:A10)
```

If your data is:

```text
15
8
23
4
19
```

the result is:

**4**

---

# 13. MAX

`MAX` finds the largest number.

```text
=MAX(A1:A10)
```

For:

```text
15
8
23
4
19
```

the result is:

**23**

---

# 14. COUNT

`COUNT` counts cells containing numbers.

Suppose:

```text
A1 = 10
A2 = 20
A3 = Apple
A4 = 30
A5 = Hello
```

Then:

```text
=COUNT(A1:A5)
```

returns:

**3**

because there are three numerical cells.

---

# 15. COUNTA

`COUNTA` counts non-empty cells.

With:

```text
A1 = 10
A2 = 20
A3 = Apple
A4 = 30
A5 = Hello
```

this:

```text
=COUNTA(A1:A5)
```

returns:

**5**

because all five cells contain something.

---

# 16. COUNT vs COUNTA

Remember:

```text
COUNT
↓
Counts numbers
```

```text
COUNTA
↓
Counts non-empty cells
```

This distinction is very important.

---

# 17. Your First Student Marks Spreadsheet

Let's make something practical.

Enter:

| Student | Math | Science | English |
| ------- | ---: | ------: | ------: |
| Ali     |   80 |      75 |      90 |
| Sara    |   95 |      88 |      92 |
| Ahmed   |   60 |      70 |      65 |
| Hamza   |   85 |      90 |      80 |
| Ayesha  |   72 |      78 |      85 |

Add:

```text
E1 = Total
F1 = Average
```

---

# 18. Calculate Total Marks

In E2 write:

```text
=SUM(B2:D2)
```

This adds:

```text
Math + Science + English
```

For Ali:

```text
80 + 75 + 90 = 245
```

---

# 19. Calculate Average Marks

In F2:

```text
=AVERAGE(B2:D2)
```

For Ali:

```text
245 / 3 = 81.666...
```

Excel may display:

```text
81.67
```

depending on formatting.

---

# 20. Use AutoFill

Now instead of writing formulas individually for every student:

1. Select E2.
2. Grab the fill handle.
3. Drag down to E6.

Then do the same for F2.

Excel will automatically create:

```text
E2 = SUM(B2:D2)
E3 = SUM(B3:D3)
E4 = SUM(B4:D4)
...
```

and:

```text
F2 = AVERAGE(B2:D2)
F3 = AVERAGE(B3:D3)
F4 = AVERAGE(B4:D4)
...
```

This is a huge productivity feature.

---

# 21. Relative References

Let's slow down here.

Suppose E2 contains:

```text
=SUM(B2:D2)
```

When you copy it one row down, Excel changes it to:

```text
=SUM(B3:D3)
```

Why?

Because `B2:D2` is a **relative reference**.

Excel assumes:

> "Move the referenced cells along with the formula."

This behavior is extremely useful.

---

# 22. Absolute References

Now imagine you have a tax rate.

```text
H1 = Tax Rate
H2 = 10%
```

Your table:

| Product  | Price |
| -------- | ----: |
| Pen      |    50 |
| Notebook |   200 |
| Bag      |  1500 |

Suppose you want tax.

You might write:

```text
=C2*$H$2
```

The `$` locks the reference.

When you copy the formula down:

```text
=C3*$H$2
=C4*$H$2
```

the product price changes, but:

```text
$H$2
```

stays fixed.

---

# 23. The Three Reference Types

### Relative

```text
A1
```

Everything can move.

### Absolute

```text
$A$1
```

Column and row are locked.

### Mixed

```text
$A1
```

Column locked, row can change.

Or:

```text
A$1
```

Row locked, column can change.

We'll practice these heavily later.

---

# 24. Percentages

Suppose:

```text
A1 = 200
```

To calculate 10%:

```text
=A1*10%
```

Result:

**20**

You could also write:

```text
=A1*0.10
```

Same mathematical idea.

---

# 25. Adding a Percentage

Suppose something costs 200 and increases by 10%.

You could use:

```text
=200*(1+10%)
```

Result:

**220**

With cells:

```text
A1 = 200
B1 = 10%
```

formula:

```text
=A1*(1+B1)
```

---

# 26. Reducing by a Percentage

If something costs 200 and gets a 10% discount:

```text
=200*(1-10%)
```

Result:

**180**

With cells:

```text
=A1*(1-B1)
```

---

# 27. IF — One of Excel's Most Important Functions

`IF` allows Excel to make a decision.

Basic structure:

```text
=IF(condition, value_if_true, value_if_false)
```

For example:

```text
=IF(A1>=50,"Pass","Fail")
```

If A1 is 70:

```text
Pass
```

If A1 is 40:

```text
Fail
```

---

# 28. Understanding the IF Formula

Take:

```text
=IF(A1>=50,"Pass","Fail")
```

Break it apart:

```text
IF
(
A1>=50,
"Pass",
"Fail"
)
```

Meaning:

> If A1 is greater than or equal to 50, show "Pass"; otherwise show "Fail."

---

# 29. Comparison Operators

You'll use these constantly.

| Operator | Meaning               |
| -------- | --------------------- |
| `=`      | Equal                 |
| `<>`     | Not equal             |
| `>`      | Greater than          |
| `<`      | Less than             |
| `>=`     | Greater than or equal |
| `<=`     | Less than or equal    |

Examples:

```text
A1>50
A1<100
A1>=50
A1<=100
A1<>0
```

---

# 30. IF With Student Marks

Suppose F2 contains average marks.

In G2:

```text
=IF(F2>=50,"Pass","Fail")
```

Then AutoFill downward.

You now have:

| Student | Average | Result |
| ------- | ------: | ------ |
| Ali     |   81.67 | Pass   |
| Sara    |   91.67 | Pass   |
| Ahmed   |      65 | Pass   |
| Hamza   |      85 | Pass   |
| Ayesha  |   78.33 | Pass   |

---

# 31. Multiple Conditions

Suppose you want:

* 80+ → A
* 70–79 → B
* 60–69 → C
* 50–59 → D
* below 50 → F

You can use multiple `IF`s.

For example:

```text
=IF(A1>=80,"A",IF(A1>=70,"B",IF(A1>=60,"C",IF(A1>=50,"D","F"))))
```

This is called a **nested IF**.

We'll later learn cleaner approaches for more complex grading systems.

---

# 32. COUNTIF

Now suppose you have:

```text
Pass
Pass
Fail
Pass
Fail
```

You want to count how many students passed.

Use:

```text
=COUNTIF(G2:G6,"Pass")
```

It counts cells matching the condition.

---

# 33. COUNTIF With Numbers

Suppose A1:A10 contains student marks.

To count scores greater than or equal to 50:

```text
=COUNTIF(A1:A10,">=50")
```

To count scores below 50:

```text
=COUNTIF(A1:A10,"<50")
```

---

# 34. SUMIF

`SUMIF` adds values that meet a condition.

Imagine:

| Product | Category    | Sales |
| ------- | ----------- | ----: |
| Pen     | Stationery  |   100 |
| Bag     | Accessories |   500 |
| Pencil  | Stationery  |    50 |
| Shoes   | Clothing    |  1000 |

To calculate total sales for Stationery:

```text
=SUMIF(B2:B5,"Stationery",C2:C5)
```

Excel finds rows where the category is Stationery, then adds the corresponding sales.

Result:

**150**

---

# 35. COUNTIF vs SUMIF

### COUNTIF

Counts matching cells.

```text
=COUNTIF(...)
```

### SUMIF

Adds corresponding values when a condition is met.

```text
=SUMIF(...)
```

---

# 36. Excel Errors

You will eventually see error messages.

Don't panic.

They're clues.

### `#DIV/0!`

Usually means you're trying to divide by zero or an empty cell that results in division by zero.

### `#VALUE!`

Often indicates incompatible data types or an inappropriate value.

### `#REF!`

A formula refers to an invalid/deleted cell reference.

### `#NAME?`

Excel doesn't recognize something in the formula, often due to a misspelled function/name.

### `#N/A`

Often means a value isn't available, especially in lookup formulas.

---

# 37. A Very Important Rule

When you see an error:

**Don't immediately delete the formula.**

Read it.

Then inspect:

1. What formula did you write?
2. Which cells does it reference?
3. Do those cells contain what you expected?
4. Did you accidentally delete or move something?
5. Did you spell the function correctly?

Troubleshooting formulas is a major Excel skill.

---

# 38. Formula vs Value

Suppose A1 contains:

```text
10
```

That's a value.

Suppose A2 contains:

```text
=A1*2
```

The formula is:

```text
=A1*2
```

The displayed result is:

```text
20
```

The cell has a formula, but Excel displays the calculated result.

You can see the formula by selecting the cell and looking at the formula bar.

---

# 39. Formula Bar vs Cell Display

Suppose B2 displays:

```text
150
```

But its formula is:

```text
=B1*C1
```

Selecting B2 lets you see the formula in the formula bar.

This is useful for understanding how a spreadsheet works.

---

# 40. Your Second Practice Project

Create this table:

| Employee | Hours | Rate | Pay |
| -------- | ----: | ---: | --: |
| Ali      |    40 |  500 |     |
| Sara     |    35 |  600 |     |
| Ahmed    |    45 |  450 |     |
| Hamza    |    30 |  700 |     |
| Ayesha   |    42 |  550 |     |

### Task 1

Calculate Pay:

```text
Hours × Rate
```

Use:

```text
=B2*C2
```

### Task 2

AutoFill the formula.

### Task 3

Calculate total payroll.

Use:

```text
=SUM(D2:D6)
```

### Task 4

Calculate average pay.

Use:

```text
=AVERAGE(D2:D6)
```

### Task 5

Find the highest pay.

Use:

```text
=MAX(D2:D6)
```

### Task 6

Find the lowest pay.

Use:

```text
=MIN(D2:D6)
```

### Task 7

Count employees whose pay is greater than 20,000.

Use:

```text
=COUNTIF(D2:D6,">20000")
```

---

# 41. What You Should Now Understand

At this point, you should know:

```text
Cell
 ↓
Reference
 ↓
Formula
 ↓
Function
 ↓
Range
 ↓
AutoFill
```

And you should understand the difference between:

```text
=A1+B1
```

and:

```text
=SUM(A1:B1)
```

as well as:

```text
A1
$A$1
$A1
A$1
```

---

# 42. The Excel Learning Path From Here

We're going to build your skills progressively:

### Level 1 — Fundamentals ✅

* cells
* rows
* columns
* worksheets
* entering data
* basic formatting

### Level 2 — Formulas & Functions ← **You are here**

* arithmetic
* references
* ranges
* SUM
* AVERAGE
* MIN
* MAX
* COUNT
* COUNTA
* IF
* COUNTIF
* SUMIF

### Level 3 — Data Management

Next:

* Excel Tables
* sorting
* filtering
* multiple criteria
* conditional formatting
* data validation
* drop-down lists
* removing duplicates
* text-to-columns
* finding/replacing
* cleaning messy data

### Level 4 — Important Functions

Then:

* `XLOOKUP`
* `VLOOKUP`
* `INDEX`
* `MATCH`
* `IFERROR`
* `SUMIFS`
* `COUNTIFS`
* `AVERAGEIF`
* `AVERAGEIFS`
* text functions
* date functions

### Level 5 — Visualization

Then:

* charts
* column charts
* line charts
* pie charts
* scatter plots
* chart formatting
* choosing the right chart

### Level 6 — Analysis

Then:

* PivotTables
* PivotCharts
* slicers
* summaries
* dashboards

### Level 7 — Advanced Excel

Eventually:

* advanced formulas
* dynamic arrays
* `FILTER`
* `SORT`
* `UNIQUE`
* `LET`
* Power Query
* data modeling
* Power Pivot
* macros/VBA

**Don't jump ahead yet.** The next lesson should be **Excel Part 3: Tables, Sorting, Filtering, Conditional Formatting, and Drop-down Lists**. That's where you'll start working with Excel like a real data-management tool rather than just a calculator.
