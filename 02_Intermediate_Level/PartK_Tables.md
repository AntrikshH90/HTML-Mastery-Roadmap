# 🅺 PART K: TABLES

## 📖 Theory (from PDF)

> HTML table is used to display data in **tabular format** (rows and columns).

| Tag | Description (from PDF) |
|-----|----------------------|
| `<table>` | Define a table. It is container for entire table |
| `<thead>` | Used to group table header content. Groups table heading rows |
| `<tbody>` | Container for table content. Groups table data rows |
| `<tfoot>` | Footer section of table |
| `<th>` | To insert header cell within row (usually bold and centered) |
| `<tr>` | To insert a row within table |
| `<td>` | To insert a table cell within row |

## Attributes (from PDF)

### Table Attributes:
| Attribute | Description (from PDF) |
|-----------|----------------------|
| `border` | Add the border around the table and its cells |
| `cellpadding` | Add space between content and cell wall |
| `cellspacing` | Add the space between cells |
| `width` | Sets width of table |
| `align` | Align the table (center, left, right) |
| `bgColor` | Background color |

### Cell Attributes (`<td>` and `<th>`):
| Attribute | Description (from PDF) |
|-----------|----------------------|
| `colspan` | Makes a cell span across **multiple columns** (horizontally) |
| `rowspan` | Makes a cell span across **multiple rows** (vertically) |

## Basic Table Example (from PDF Page 7)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Table</title>
</head>
<body>
    <section>
        <table border="1">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Age</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>John</td>
                    <td>25</td>
                </tr>
                <tr>
                    <td>Jane</td>
                    <td>24</td>
                </tr>
                <tr>
                    <td>Jack</td>
                    <td>23</td>
                </tr>
            </tbody>
        </table>
    </section>
</body>
</html>
```

## Table with All Attributes (from PDF Page 39)

```html
<table border="2" cellpadding="10" cellspacing="10" 
       width="300" align="center" bgColor="white">
    <thead>
        <tr>
            <th>Id</th>
            <th>Name</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>101</td>
            <td>Satyajit</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Pranav</td>
        </tr>
        <tr>
            <td colspan="2" rowspan="2">Spanning cell</td>
            <td>Extra</td>
        </tr>
    </tbody>
</table>
```

## Complete Semantic Table (Modern Best Practice)

```html
<table>
    <caption>Employee Directory 2025</caption>
    
    <colgroup>
        <col style="background-color: #f0f0f0">
        <col span="2">
        <col style="background-color: #e0ffe0">
    </colgroup>
    
    <thead>
        <tr>
            <th scope="col">ID</th>
            <th scope="col">Name</th>
            <th scope="col">Department</th>
            <th scope="col">Salary</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td>001</td>
            <td>Alice Johnson</td>
            <td>Engineering</td>
            <td>$95,000</td>
        </tr>
        <tr>
            <td>002</td>
            <td>Bob Smith</td>
            <td>Marketing</td>
            <td>$75,000</td>
        </tr>
    </tbody>
    
    <tfoot>
        <tr>
            <td colspan="3"><strong>Total</strong></td>
            <td><strong>$170,000</strong></td>
        </tr>
    </tfoot>
</table>
```

## Spanning Rows & Columns

```html
<table border="1">
    <tr>
        <th colspan="3">Student Schedule</th>  <!-- Spans 3 columns -->
    </tr>
    <tr>
        <th>Time</th>
        <th>Monday</th>
        <th>Tuesday</th>
    </tr>
    <tr>
        <td>9:00</td>
        <td rowspan="2">Math (Double Period)</td>  <!-- Spans 2 rows -->
        <td>English</td>
    </tr>
    <tr>
        <td>10:00</td>
        <!-- Math continues from above -->
        <td>Science</td>
    </tr>
</table>
```

> ⚠️ **Important:** Don't use tables for page layout! Tables are for **tabular data only**. Use CSS Grid/Flexbox for layouts.

---

