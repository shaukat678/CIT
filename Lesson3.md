---
---

# 📊 Excel for Complete Beginners — Part 1

## 1. What Is Excel?

**Microsoft Excel** is a spreadsheet program.

It's mainly used to:

* organize information
* perform calculations
* analyze data
* make tables
* create charts
* track expenses
* manage lists
* build reports
* work with numbers

You can think of Excel as a combination of:

> **Notebook + Calculator + Table + Database-like tools + Charts**

---

# 2. What Is a Spreadsheet?

A spreadsheet is a grid made of **rows and columns**.

Imagine a giant piece of graph paper:

```text
       A       B       C       D
    ┌───────┬───────┬───────┬───────┐
1   │       │       │       │       │
    ├───────┼───────┼───────┼───────┤
2   │       │       │       │       │
    ├───────┼───────┼───────┼───────┤
3   │       │       │       │       │
    ├───────┼───────┼───────┼───────┤
4   │       │       │       │       │
    └───────┴───────┴───────┴───────┘
```

Columns go:

**A, B, C, D...**

Rows go:

**1, 2, 3, 4...**

---

# 3. What Is a Cell?

The individual boxes in Excel are called **cells**.

Every cell has an address.

For example:

```text
A1
```

means:

> Column A + Row 1

Another example:

```text
C7
```

means:

> Column C + Row 7

This is one of the most important Excel concepts.

---

# 4. The Active Cell

The cell you currently have selected is called the **active cell**.

If you click:

```text
B4
```

B4 becomes the active cell.

You'll usually see a border around it.

Whatever you type will normally go into that cell.

---

# 5. Columns

Columns run **vertically**.

```text
A
│
│
│
│
```

They are identified with letters:

```text
A B C D E F G ...
```

---

# 6. Rows

Rows run **horizontally**.

```text
1 ─────────────────
2 ─────────────────
3 ─────────────────
4 ─────────────────
```

They are identified with numbers.

---

# 7. Cell Addresses

Combine the column letter and row number.

Examples:

```text
A1
B3
D10
F25
Z100
```

Notice:

**Column first → row second**

So:

```text
C8
```

means:

> Column C, row 8.

---

# 8. Entering Data

Click cell A1.

Type:

```text
Apple
```

Press **Enter**.

You've entered data into A1.

Now click A2 and type:

```text
Banana
```

You might have:

```text
       A
   ┌─────────┐
1  │ Apple   │
   ├─────────┤
2  │ Banana  │
   ├─────────┤
3  │         │
```

---

# 9. Different Types of Data

Excel can work with different kinds of information.

### Text

```text
Apple
John
Pakistan
Computer
```

### Numbers

```text
10
250
3.14
-50
```

### Dates

```text
19/09/2026
```

### Times

```text
10:30 AM
```

### Formulas

```text
=10+20
```

Understanding the difference is important.

---

# 10. Editing a Cell

Suppose A1 contains:

```text
Apple
```

You can:

### Double-click the cell

Then edit its contents.

Or select the cell and use the **formula bar**.

Or select the cell and start typing to replace its contents.

---

# 11. Deleting Cell Contents

Select a cell and press:

**Delete**

This removes the cell's contents.

It doesn't necessarily remove the cell itself.

The grid remains.

---

# 12. Moving Around

You can use:

**Arrow keys**

to move around.

For example:

```text
↑
← ↓ →
```

You can also use:

**Enter**

to move to another cell according to Excel's current behavior.

---

# 13. The Formula Bar

Near the top of Excel you'll find the **formula bar**.

If A1 contains:

```text
Hello
```

selecting A1 lets you see its contents in the formula bar.

This becomes especially important when cells contain formulas.

For example:

```text
=SUM(B2:B10)
```

---

# 14. Excel Files

Modern Excel workbooks commonly use:

```text
.xlsx
```

An Excel file is called a **workbook**.

Inside the workbook are **worksheets**.

Think:

```text
Workbook
│
├── Sheet1
├── Sheet2
└── Sheet3
```

---

# 15. Workbook vs Worksheet

This is another important distinction.

### Workbook

The entire Excel file.

### Worksheet

An individual spreadsheet inside that file.

For example:

```text
Budget.xlsx
│
├── January
├── February
└── March
```

`Budget.xlsx` = workbook.

`January` = worksheet.

---

# 16. Creating Your First Table

Let's make something useful.

Enter this:

```text
A1: Product
B1: Price
C1: Quantity
D1: Total

A2: Pen
B2: 50
C2: 3

A3: Notebook
B3: 200
C3: 2

A4: Bag
B4: 1500
C4: 1
```

You now have:

| Product  | Price | Quantity | Total |
| -------- | ----: | -------: | ----: |
| Pen      |    50 |        3 |       |
| Notebook |   200 |        2 |       |
| Bag      |  1500 |        1 |       |

Now we'll make Excel calculate the totals.

---

# 17. What Is a Formula?

A formula tells Excel to perform a calculation.

**Important rule:**

Excel formulas normally begin with:

```text
=
```

For example:

```text
=10+20
```

Excel calculates:

```text
30
```

---

# 18. Basic Arithmetic

Excel can perform:

### Addition

```text
=10+5
```

### Subtraction

```text
=10-5
```

### Multiplication

```text
=10*5
```

Notice multiplication uses:

```text
*
```

not `×`.

### Division

```text
=10/5
```

---

# 19. Using Cell References

Here's where Excel becomes powerful.

Suppose:

```text
A1 = 10
A2 = 20
```

In A3 write:

```text
=A1+A2
```

Excel gives:

```text
30
```

Instead of manually typing:

```text
=10+20
```

you're telling Excel:

> Take the value from A1 and add the value from A2.

---

# 20. Our First Real Formula

Return to our shopping table.

In D2 write:

```text
=B2*C2
```

Excel calculates:

```text
50 × 3 = 150
```

So D2 becomes:

```text
150
```

For Notebook:

```text
=B3*C3
```

gives:

```text
400
```

For Bag:

```text
=B4*C4
```

gives:

```text
1500
```

Now:

| Product  | Price | Quantity | Total |
| -------- | ----: | -------: | ----: |
| Pen      |    50 |        3 |   150 |
| Notebook |   200 |        2 |   400 |
| Bag      |  1500 |        1 |  1500 |

---

# 21. The Amazing Part: Fill Handle

You don't need to manually type:

```text
=B2*C2
=B3*C3
=B4*C4
```

Instead:

1. Enter `=B2*C2` in D2.
2. Select D2.
3. Find the tiny square at the bottom-right corner of the selected cell.
4. Drag it downward.

Excel automatically adjusts the references.

You'll get:

```text
D2 = B2*C2
D3 = B3*C3
D4 = B4*C4
```

This is called **AutoFill**.

You'll use it constantly.

---

# 22. Why Did Excel Change B2 to B3?

Because Excel uses **relative references** by default.

When you copy:

```text
=B2*C2
```

one row down, Excel interprets it as:

```text
=B3*C3
```

It adjusts the references according to the new position.

This concept will become extremely important later.

---

# 23. SUM

Suppose you want the total of the Total column.

You could write:

```text
=D2+D3+D4
```

But Excel has a better function:

```text
=SUM(D2:D4)
```

This means:

> Add everything from D2 through D4.

Result:

```text
2050
```

---

# 24. What Does the Colon Mean?

In Excel:

```text
D2:D4
```

means:

```text
D2
D3
D4
```

It's a **range**.

Another example:

```text
A1:A10
```

means all cells from A1 through A10.

---

# 25. Functions

A **function** is a built-in Excel operation.

Examples:

```text
=SUM(...)
=AVERAGE(...)
=MIN(...)
=MAX(...)
=COUNT(...)
```

You don't need to memorize everything.

You'll learn functions as you need them.

---

# 26. AVERAGE

Suppose:

```text
A1 = 10
A2 = 20
A3 = 30
```

Use:

```text
=AVERAGE(A1:A3)
```

Result:

```text
20
```

It calculates the arithmetic average.

---

# 27. MIN

```text
=MIN(A1:A10)
```

returns the smallest number in the range.

---

# 28. MAX

```text
=MAX(A1:A10)
```

returns the largest number.

---

# 29. COUNT

```text
=COUNT(A1:A10)
```

counts cells containing numbers.

This is different from counting every non-empty cell.

That distinction matters later.

---

# 30. Formatting

Excel isn't just about calculations.

You can change how information looks.

For example:

* bold
* italic
* font size
* alignment
* borders
* number formats
* colors
* column width
* row height

Formatting changes the **appearance**, not normally the underlying value.

---

# 31. Bold Headers

Select:

```text
A1:D1
```

and click **Bold**.

Your headers now stand out.

---

# 32. Column Width

Sometimes:

```text
Product
```

doesn't fit.

You can adjust the column width.

A common method is to position your mouse between two column headings and drag.

You can also use AutoFit where appropriate.

---

# 33. Number Formatting

Suppose B2 contains:

```text
50
```

You can display it as a currency amount.

The underlying value can remain:

```text
50
```

while the display becomes something like:

```text
Rs 50.00
```

depending on the chosen currency/format.

This distinction is important:

> **Formatting can change how a value looks without changing the value itself.**

---

# 34. Decimal Places

A number like:

```text
25
```

can be displayed as:

```text
25.00
```

or:

```text
25.000
```

depending on the number format.

Again, the underlying value may still be 25.

---

# 35. Sorting

Suppose you have:

| Name  | Score |
| ----- | ----: |
| Ali   |    70 |
| Sara  |    95 |
| Ahmed |    82 |

You can sort by Score.

For example:

```text
95
82
70
```

This is useful when working with:

* marks
* prices
* dates
* names
* sales
* rankings

Be careful to sort the **whole table**, not just one column, unless you intentionally want to separate the data.

---

# 36. Filtering

Filtering lets you temporarily show only rows that meet certain conditions.

For example:

| Student | Grade |
| ------- | ----: |
| Ali     |    90 |
| Sara    |    65 |
| Ahmed   |    82 |
| Hamza   |    95 |

You could filter to show only students with grades above a chosen threshold.

The other rows aren't necessarily deleted—they're simply hidden from the current filtered view.

---

# 37. Freeze Panes

Imagine a table with 1,000 rows.

When you scroll down, the headers disappear.

**Freeze Panes** can keep important rows/columns visible while you scroll.

This is extremely useful for large spreadsheets.

---

# 38. The Most Important Excel Concept: References

Excel formulas can refer to cells.

There are three major types you'll eventually need:

### Relative

```text
A1
```

### Absolute

```text
$A$1
```

### Mixed

```text
$A1
A$1
```

For now, remember:

> `$` can lock a row, column, or both when copying formulas.

We'll go deeply into this later.

---

# 39. Example of Why Absolute References Matter

Suppose:

```text
A1 = Price
B1 = Tax Rate

A2 = 100
B2 = 10%
```

You want to calculate tax.

You might eventually have many rows:

```text
A2 = 100
A3 = 200
A4 = 300
```

and one tax rate stored in:

```text
B1
```

You don't want Excel to change B1 to B2, B3, B4 as you copy the formula.

So you can use:

```text
=A2*$B$1
```

`A2` changes when copied.

`$B$1` stays fixed.

This is one of the most useful Excel skills you'll learn.

---

# 40. Excel's Core Vocabulary

Learn these words:

| Term        | Meaning                    |
| ----------- | -------------------------- |
| Workbook    | Excel file                 |
| Worksheet   | Sheet inside workbook      |
| Cell        | Individual grid location   |
| Row         | Horizontal line            |
| Column      | Vertical line              |
| Range       | Group of cells             |
| Formula     | Calculation you write      |
| Function    | Built-in calculation       |
| Reference   | Address used in a formula  |
| Fill Handle | Tool for copying/filling   |
| Formula Bar | Area showing cell contents |
| Filter      | Shows matching records     |
| Sort        | Reorders data              |
| Formatting  | Changes appearance         |

---

# 41. Your First Excel Practice Project

Create a workbook called:

```text
Excel_Practice.xlsx
```

Create a sheet called:

```text
Shopping
```

Enter:

| Product  | Price | Quantity | Total |
| -------- | ----: | -------: | ----: |
| Pen      |    50 |        3 |       |
| Notebook |   200 |        2 |       |
| Bag      |  1500 |        1 |       |
| Pencil   |    30 |        5 |       |
| Bottle   |   500 |        2 |       |

Then:

### Task 1

Calculate Total:

```text
Price × Quantity
```

### Task 2

Use AutoFill.

### Task 3

Calculate the grand total using:

```text
SUM
```

### Task 4

Make the headers bold.

### Task 5

Format the prices as currency.

### Task 6

Sort the products by price.

### Task 7

Change column widths so everything is readable.

---

# 42. The Most Important Beginner Rule

Don't try to memorize hundreds of Excel functions.

Instead, learn this pattern:

> **Data → Cell references → Formula → Function → Copy → Format → Analyze**

Once this becomes natural, Excel starts making much more sense.

---

## What we'll learn next

The next stage should be **Excel Part 2: formulas and functions**, where we'll go from simple arithmetic into:

* `SUM`
* `AVERAGE`
* `MIN`
* `MAX`
* `COUNT`
* `COUNTA`
* `COUNTIF`
* `SUMIF`
* `IF`
* nested `IF`
* relative vs absolute references
* copying formulas correctly
* percentages
* dates
* text operations
* error messages
* practical exercises

Then we'll move into **tables, sorting/filtering, charts, PivotTables, XLOOKUP, data cleaning, and eventually advanced Excel**.
