# DAX Functions Cheat Sheet

A comprehensive reference for DAX (Data Analysis Expressions) functions used in Power BI, Excel, and Analysis Services. This repository contains a categorized list of essential DAX functions along with their descriptions.

## 📌 Categories
- [Aggregation](#aggregation)
- [Iterator](#iterator)
- [Date & Time](#date--time)
- [Logical](#logical)
- [Text](#text)
- [Relationship](#relationship)
- [Filter](#filter)
- [Table Manipulation](#table-manipulation)
- [Time Intelligence](#time-intelligence)
- [Information](#information)

## Aggregation

- `SUM(column)` - Adds up the values in a column.
- `AVERAGE(column)` - Calculates the average of the values in a column.
- `MAX(column)` - Returns the largest value in a column.
- `MIN(column)` - Returns the smallest value in a column.
- `COUNT(column)` - Counts the number of non-blank values in a column.
- `DISTINCTCOUNT(column)` - Counts the number of distinct values in a column.
- `DIVIDE(numerator, denominator, alternateResult)` - Performs division with an alternate result if the denominator is 0.
- `RANKX(table, expression, [value], [order], [ties])` - Returns the ranking of a number in a list.

## Iterator
- `SUMX(table, expression)` - Returns the sum of an expression evaluated for each row in a table.
- `AVERAGEX(table, expression)` - Evaluates the arithmetic mean for each row in a table.
- `MAXX(table, expression)` - Returns the maximum result from evaluating an expression in a table.
- `MINX(table, expression)` - Returns the minimum result from evaluating an expression in a table.
- `COUNTX(table, expression)` - Counts the number of rows where the expression is not blank.

## Date & Time
- `CALENDAR(start_date, end_date)` - Returns a single-column table of dates.
- `DATE(year, month, day)` - Returns a date in datetime format.
- `DATEDIFF(date_1, date_2, interval)` - Returns the difference between two dates.
- `DAY(date)` - Returns the day of the month.
- `MONTH(date)` - Returns the month number.
- `YEAR(date)` - Returns the year.
- `WEEKNUM(date)` - Returns the week number in a year.
- `QUARTER(date)` - Returns the quarter number of the year.

## Logical
- `IF(condition, value_if_true, [value_if_false])` - Returns a value based on a condition.
- `AND(condition1, condition2)` - Returns TRUE if both conditions are met.
- `OR(condition1, condition2)` - Returns TRUE if at least one condition is met.
- `NOT(condition)` - Returns the opposite boolean value.
- `SWITCH(expression, value1, result1, [value2, result2, ...], [else])` - Evaluates an expression against a list of values and returns a corresponding result.
- `IFERROR(value, value_if_error)` - Returns `value_if_error` if the first expression results in an error.

## Text
- `CONCATENATE(text1, text2)` - Joins two text strings.
- `FORMAT(value, format)` - Converts a value into a formatted text.
- `LEFT(text, num_chars)` - Extracts characters from the start of a string.
- `RIGHT(text, num_chars)` - Extracts characters from the end of a string.
- `LEN(text)` - Returns the length of a string.
- `UPPER(text)` - Converts a string to uppercase.
- `LOWER(text)` - Converts a string to lowercase.
- `TRIM(text)` - Removes extra spaces from a text string.
- `SUBSTITUTE(text, old_text, new_text, [instance_num])` - Replaces existing text with new text.

## Relationship
- `CROSSFILTER(left_column, right_column, crossfiltertype)` - Defines the cross-filtering direction.
- `RELATED(column)` - Returns a related value from another table.

## Filter
- `ALL(table | column, ...)` - Returns all rows, ignoring filters.
- `ALLEXCEPT(table, column, ...)` - Returns all rows except those affected by specified filters.
- `FILTER(table, filter_expression)` - Returns a subset of a table.
- `CALCULATE(expression, filter1, filter2, ...)` - Evaluates an expression in a modified filter context.
- `REMOVEFILTERS(table | column, ...)` - Clears all filters from designated columns or tables.

## Table Manipulation
- `ADDCOLUMNS(table, name, expression, ...)` - Adds calculated columns to a table.
- `SELECTCOLUMNS(table, name, expression, ...)` - Selects specified columns from a table.
- `DISTINCT(table)` - Returns a table with duplicate rows removed.
- `SUMMARIZE(table, groupBy_column, ..., name, expression, ...)` - Groups data and creates aggregations.
- `INTERSECT(left_table, right_table)` - Returns common rows between two tables.
- `UNION(table1, table2, ...)` - Combines multiple tables with matching columns.
- `NATURALINNERJOIN(left_table, right_table)` - Joins tables using an inner join.
- `NATURALLEFTOUTERJOIN(left_table, right_table)` - Joins tables using a left outer join.

## Time Intelligence
- `DATEADD(dates, number_of_intervals, interval)` - Moves a date by a specified interval.
- `DATESBETWEEN(dates, start_date, end_date)` - Returns dates between two specified dates.
- `TOTALYTD(expression, dates, [filter], [year_end_date])` - Returns the year-to-date value.
- `SAMEPERIODLASTYEAR(dates)` - Returns a column of dates shifted one year back.
- `STARTOFMONTH(dates)` - Returns the start of the month.
- `ENDOFMONTH(dates)` - Returns the end of the month.

## Information
- `ISBLANK(value)` - Checks if a value is blank.
- `ISNUMBER(value)` - Checks if a value is a number.
- `ISLOGICAL(value)` - Checks if a value is a boolean.
- `ISFILTERED(column)` - Returns TRUE if a column is filtered.
- `ISCROSSFILTERED(column)` - Returns TRUE if a column has cross-filters.
- `HASONEVALUE(column)` - Returns TRUE if a column has a single value in the filter context.
- `USERPRINCIPALNAME()` - Returns the current user's name.

---

### 📚 Learn More
Visit [Microsoft DAX Guide](https://learn.microsoft.com/en-us/dax/) for official documentation.

### 📌 Contributions
Feel free to contribute by adding more functions, improving descriptions, or fixing issues.

---
**Maintained by:** *[Antonio Figueiredo](https://github.com/amgfigueiredo)*
