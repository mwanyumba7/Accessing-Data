# Visual Quality Assessment Of The Data Sets
The following few quality concerns in our data sets were discovered by a visual inspection of our datasets.

**Issue 1: hba1c Change**
For this clinical trial data, our key metric is the change in hba1c, or `hba1c_change` in the `treatments` table. It is important data that the data in this column is clean but some of these entries are empty, NaN, or missing values. This is a data quality issue. We can document it as:

> treatments table missing hba1c changes.

**Issue 2: Zip Codes**
The entries in the `zip_code` column in the `patients` table have decimals. Some zip codes have five digits before the decimal and others have four before the decimal. This data was probably added from a spreadsheet that typed the zip codes as numbers, adding the decimal and lopping off the leading 0.
The two issues are the data type and the inconsistency of the data. We can document them as:

> zip code is a float not a string ****zip code has four digits sometimes

**Issue 3: Height**
In the `patients` table the recorded `height` for Tim Neudorf. His recorded height is 27 inches, or two feet and three inches tall, which inconsistent with his weight and body mass index. We can document this as:

> Tim Neudorf height is 27 in instead of 72 in

Again, we'll document this issue. This is important in terms of the clinical trial because of the reporting of average metrics, such as average height and weight.

**Issue 4: States**
In the `patients` table, the state column uses both full state name abbreviations to represent the states. We should document this to improve consistency.

> full state names sometimes, abbreviations other times

After visual assessment, our Quality Assessment documentation should look like this:

> **Quality**
    - *treatments* table - missing HbA1c changes
    - *patients* table - zip code is a float not a string
    - *patients* table - zip code has four digits sometimes
    - *patients* table - Tim Neudorf height is 27 in instead of 72 in
    - *patients* table - full state names sometimes, abbreviations other tim*es*




