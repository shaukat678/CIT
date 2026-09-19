# Excel Part 3 — Tables, Sorting, Filtering & Data Management

Now we’ll learn how to turn ordinary data into **organized, searchable, professional Excel data**.

---

## 1. What is an Excel Table?

Suppose you have:

| Name   | Subject | Marks | Class |
| ------ | ------- | ----: | ----- |
| Ali    | Math    |    85 | 9     |
| Sara   | Math    |    92 | 9     |
| Ahmed  | Math    |    67 | 9     |
| Ayesha | Math    |    78 | 9     |

This is just a normal range of cells.

An **Excel Table** is a special version of this data that gives you useful features automatically:

* Filter buttons
* Automatic formatting
* Automatic expansion when you add rows
* Structured formulas
* Easier data management

### Create a Table

1. Select your data, including the headings.
2. Press **Ctrl + T**.
3. Excel asks whether your table has headers.
4. Make sure **My table has headers** is checked.
5. Click **OK**.

Your data is now an Excel Table.

---

# 2. Why Tables Are Useful

Imagine you have 5,000 rows.

Without a table, managing that data can become difficult.

With a table, Excel can automatically give you:

**Name ▼ | Subject ▼ | Marks ▼ | Class ▼**

Those little arrows are **filter buttons**.

You can click one and tell Excel:

> "Show me only students whose marks are above 80."

---

# 3. Sorting

**Sorting** means arranging data in an order.

For example:

### Before

| Name   | Marks |
| ------ | ----: |
| Ali    |    65 |
| Sara   |    92 |
| Ahmed  |    74 |
| Ayesha |    88 |

### Sort Marks from smallest to largest

| Name   | Marks |
| ------ | ----: |
| Ali    |    65 |
| Ahmed  |    74 |
| Ayesha |    88 |
| Sara   |    92 |

This is called **ascending order**.

### Largest to smallest

| Name   | Marks |
| ------ | ----: |
| Sara   |    92 |
| Ayesha |    88 |
| Ahmed  |    74 |
| Ali    |    65 |

This is **descending order**.

### How to sort

Click the filter arrow on the **Marks** column.

You'll see options such as:

* Sort Smallest to Largest
* Sort Largest to Smallest

---

# 4. Sorting Text

Sorting doesn't only work with numbers.

Suppose:

| Name  |
| ----- |
| Sara  |
| Ali   |
| Ahmed |
| Zain  |

You can sort:

**A → Z**

Result:

| Name  |
| ----- |
| Ahmed |
| Ali   |
| Sara  |
| Zain  |

Or:

**Z → A**

---

# 5. Important Warning About Sorting

Suppose your table is:

| Name | Math | English |
| ---- | ---: | ------: |
| Ali  |   80 |      75 |
| Sara |   95 |      88 |

If you sort only the **Math column manually**, you could accidentally separate people's names from their marks.

That's bad.

When working with related data, sort the **whole table**, not isolated cells.

Excel Tables help prevent this problem.

---

# 6. Filtering

Sorting changes the order.

**Filtering hides data you don't currently want to see.**

For example:

| Name   | Marks |
| ------ | ----: |
| Ali    |    45 |
| Sara   |    92 |
| Ahmed  |    67 |
| Ayesha |    88 |

Suppose you only want students with marks **80 or higher**.

Use the filter on Marks:

**Number Filters → Greater Than or Equal To → 80**

Excel might show:

| Name   | Marks |
| ------ | ----: |
| Sara   |    92 |
| Ayesha |    88 |

The other rows haven't been deleted.

They're simply **hidden by the filter**.

---

# 7. Clearing a Filter

After filtering, you may want to see everything again.

Click the filter arrow and choose:

**Clear Filter**

Your original data appears again.

---

# 8. Filtering by Text

Suppose you have:

| Name   | Department |
| ------ | ---------- |
| Ali    | Sales      |
| Sara   | IT         |
| Ahmed  | Sales      |
| Ayesha | HR         |

You can filter Department to show only:

**Sales**

Result:

| Name  | Department |
| ----- | ---------- |
| Ali   | Sales      |
| Ahmed | Sales      |

---

# 9. Multiple Filters

This is extremely useful.

Suppose you have:

| Name   | Department | Salary |
| ------ | ---------- | -----: |
| Ali    | Sales      |  50000 |
| Sara   | IT         |  80000 |
| Ahmed  | Sales      |  65000 |
| Ayesha | HR         |  70000 |
| Zain   | IT         |  90000 |

You can filter:

**Department = IT**

AND

**Salary > 75,000**

Result:

| Name | Department | Salary |
| ---- | ---------- | -----: |
| Sara | IT         |  80000 |
| Zain | IT         |  90000 |

Excel applies both conditions.

---

# 10. Conditional Formatting

This is one of Excel's most useful features.

**Conditional formatting automatically changes a cell's appearance when a condition is true.**

For example:

> If marks are below 50, make them visually stand out.

Suppose:

| Student | Marks |
| ------- | ----: |
| Ali     |    85 |
| Sara    |    42 |
| Ahmed   |    73 |
| Ayesha  |    35 |

Select the Marks column.

Go to:

**Home → Conditional Formatting**

You can choose things such as:

* Highlight Cells Rules
* Greater Than
* Less Than
* Between
* Duplicate Values
* Data Bars
* Color Scales
* Icon Sets

For example:

**Less Than → 50**

Excel highlights the marks below 50.

---

# 11. Conditional Formatting With Color Scales

Suppose you have:

| Student | Marks |
| ------- | ----: |
| Ali     |    95 |
| Sara    |    72 |
| Ahmed   |    45 |
| Ayesha  |    88 |

A **Color Scale** can visually show lower and higher values.

This makes patterns easier to notice without manually examining every number.

---

# 12. Data Bars

Another useful option is **Data Bars**.

Suppose:

| Student | Sales |
| ------- | ----: |
| Ali     |   200 |
| Sara    |   800 |
| Ahmed   |   500 |
| Ayesha  |  1000 |

Data bars display a bar inside each cell.

A larger number gets a longer bar.

So you can quickly see which values are larger.

---

# 13. Drop-Down Lists

Now we're getting into **data validation**.

Suppose you're creating a form where someone needs to select a department.

Instead of allowing them to type:

* Sales
* sales
* SALES
* Sale
* Salse

you can give them a controlled list.

For example:

**Department ▼**

Options:

* Sales
* IT
* HR
* Finance

---

# 14. Creating a Drop-Down List

Let's say cell **B2** should contain the department.

Select B2.

Go to:

**Data → Data Validation**

Choose:

**Allow: List**

Then provide the options, such as:

`Sales,IT,HR,Finance`

Click **OK**.

Now B2 has a drop-down arrow.

The user chooses instead of typing.

---

# 15. Why Drop-Down Lists Matter

This is about **data quality**.

Imagine 10,000 employee records.

If people type departments manually, you might get:

```text
IT
it
Information Technology
I.T.
It
```

Excel treats these as different text values.

A drop-down list helps keep the data consistent.

---

# 16. Removing Duplicates

Sometimes data contains repeated records.

Example:

| Student ID | Name  |
| ---------- | ----- |
| 101        | Ali   |
| 102        | Sara  |
| 101        | Ali   |
| 103        | Ahmed |

Student 101 appears twice.

Excel has a feature:

**Data → Remove Duplicates**

Select the relevant columns.

Excel checks for duplicate rows and lets you remove them.

### Important

Be careful with this feature.

You should understand **what counts as a duplicate** before deleting anything.

---

# 17. Find and Replace

Imagine a spreadsheet contains:

```text
Karachi
Karachi
Karachi
Karachi
```

You discover that you want to replace `Karachi` with something else.

Press:

**Ctrl + H**

This opens **Find and Replace**.

You can specify:

**Find what:**
`Karachi`

**Replace with:**
`Example`

Then choose **Replace All** if you're sure.

---

# 18. Find

If you only want to locate something:

**Ctrl + F**

For example, search for:

`Sara`

Excel finds matching cells.

This becomes extremely useful with large spreadsheets.

---

# 19. Text to Columns

This is another important data-cleaning tool.

Suppose one column contains:

```text
Ali Khan
Sara Ahmed
Ahmed Raza
```

Maybe you want:

| First Name | Last Name |
| ---------- | --------- |
| Ali        | Khan      |
| Sara       | Ahmed     |
| Ahmed      | Raza      |

You can use:

**Data → Text to Columns**

Excel can split the information based on a delimiter such as:

* Space
* Comma
* Tab
* Semicolon

---

# 20. A Practical Project

Let's build a small **Student Management Table**.

Enter this into Excel:

| Student ID | Name   | Class | Subject | Marks | Status |
| ---------: | ------ | ----: | ------- | ----: | ------ |
|        101 | Ali    |     9 | Math    |    85 |        |
|        102 | Sara   |     9 | Math    |    42 |        |
|        103 | Ahmed  |     9 | Math    |    73 |        |
|        104 | Ayesha |     9 | Math    |    91 |        |
|        105 | Zain   |     9 | Math    |    56 |        |
|        106 | Hina   |     9 | Math    |    38 |        |

---

## Exercise 1 — Turn it into a Table

Select everything.

Press:

**Ctrl + T**

Confirm:

**My table has headers**

---

## Exercise 2 — Sort

Sort **Marks** from:

**Largest → Smallest**

You should see the highest-scoring student at the top.

---

## Exercise 3 — Filter

Filter Marks to show only:

**Marks ≥ 70**

Now only students with 70 or higher should be visible.

---

## Exercise 4 — Conditional Formatting

Apply conditional formatting to Marks:

**Less Than 50**

This should make the low marks visually noticeable.

---

## Exercise 5 — Drop-Down List

Create another column called:

**Grade**

Give it a drop-down list containing:

```text
A
B
C
D
F
```

Now you can select a grade from the list instead of typing it.

---

# 21. A Very Important Excel Concept

At this point, understand the difference:

### Formula

Calculates something.

Example:

```excel
=A2+B2
```

### Function

A built-in calculation.

Example:

```excel
=SUM(A2:A10)
```

### Sort

Changes the **order** of data.

### Filter

**Hides** data that doesn't match your conditions.

### Conditional Formatting

Changes how cells **look** based on conditions.

### Data Validation

Controls what users are **allowed to enter**.

### Table

Turns a range into a structured data object with useful built-in features.

---

# 22. Your Excel Skill Tree So Far

You now know:

**Level 1**

* Cells
* Rows
* Columns
* Worksheets
* Workbooks
* Data entry
* Formatting

↓

**Level 2**

* Formulas
* Cell references
* Functions
* `SUM`
* `AVERAGE`
* `MIN`
* `MAX`
* `COUNT`
* `IF`
* `COUNTIF`
* `SUMIF`
* Absolute references

↓

**Level 3**

* Excel Tables
* Sorting
* Filtering
* Conditional formatting
* Data validation
* Drop-down lists
* Remove duplicates
* Find & Replace
* Text to Columns

### Next: Excel Part 4

We'll move into some of the **most important Excel functions used in real work**, including:

* `XLOOKUP`
* `VLOOKUP`
* `INDEX`
* `MATCH`
* `SUMIFS`
* `COUNTIFS`
* `AVERAGEIF`
* `IFERROR`
* Text functions
* Date functions

These are where Excel starts becoming much more powerful.
