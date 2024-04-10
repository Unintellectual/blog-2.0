---
title: "Tabular"
description: "Tabluation tool made in Go inspired by Tabulate Library in python"
image:
  url: "/portfolio-2023.png"
  alt: "Tabular Image"
worksImage1:
  url: "/image-1.webp"
  alt: "Tabular Github"
worksImage2:
  url: "/image-2.webp"
  alt: "Tabular Example"
platform: Library
stack:  Go, GoTest
website: https://github.com/Unintellectual/tabular.git
---
Tabular is a versatile Go library designed to simplify the elegant formatting of tabular data.

Supported data types:

- 2D Array of `Int`, `Int64`, `Float64`, `String`, `interface{}`
- Map of `String`, `interface{}` (Keys will be used as header)

### Examples:

```go
t := gotabular.Create([][]string{STRING_ARRAY, STRING_ARRAY})

t.SetHeaders(HEADERS) // If not headers are set, the first row will be used.

t.SetEmptyString("None") // Set what will be printed in the empty cell

rendered_string := t.Render("simple") // Render() will return a string

Simple Table
----------------------  ----------------------  ----------------------  -------------  -------------
             Header 1                Header 2                Header 3       Header 4       Header 5
----------------------  ----------------------  ----------------------  -------------  -------------
          test string           test string 2                    test            row           bndr

          test string           test string 2                    test            row           bndr

    4th element empty       4th element empty       4th element empty           None           None
----------------------  ----------------------  ----------------------  -------------  -------------

Grid Table (Align Right)
+-------------+-------------+-------------+-------------+-------------+
|    Header 1 |    Header 2 |    Header 3 |    Header 4 |    Header 5 |
+=============+=============+=============+=============+=============+
|       10.01 |      12.002 |      -123.5 |    20.00005 |        1.01 |
+-------------+-------------+-------------+-------------+-------------+
|       10.01 |      12.002 |      -123.5 |    20.00005 |        1.01 |
+-------------+-------------+-------------+-------------+-------------+
|       10.01 |      12.002 |      -123.5 |    20.00005 |        None |
+-------------+-------------+-------------+-------------+-------------+

Padded Headers:
+----------------------+----------------------+----------------------+-------------+-------------+
|                      |             Header 1 |             header 2 |    header 3 |    header 4 |
+======================+======================+======================+=============+=============+
|          test string |        test string 2 |                 test |         row |        bndr |
+----------------------+----------------------+----------------------+-------------+-------------+
|          test string |        test string 2 |                 test |         row |        bndr |
+----------------------+----------------------+----------------------+-------------+-------------+
|    4th element empty |    4th element empty |    4th element empty |        None |        None |
+----------------------+----------------------+----------------------+-------------+-------------+

Align Center:
+-------------+-------------+-------------+-------------+-------------+
|   Header 1  |   Header 2  |   Header 3  |   Header 4  |   Header 5  |
+=============+=============+=============+=============+=============+
|    10.01    |    12.002   |    -123.5   |   20.00005  |     1.01    |
+-------------+-------------+-------------+-------------+-------------+
|    10.01    |    12.002   |    -123.5   |   20.00005  |     1.01    |
+-------------+-------------+-------------+-------------+-------------+
|    10.01    |    12.002   |    -123.5   |   20.00005  |     1.01    |
+-------------+-------------+-------------+-------------+-------------+

Align Left:
+-------------+-------------+-------------+-------------+-------------+
| Header 1    | Header 2    | Header 3    | Header 4    | Header 5    |
+=============+=============+=============+=============+=============+
| 10.01       | 12.002      | -123.5      | 20.00005    | 1.01        |
+-------------+-------------+-------------+-------------+-------------+
| 10.01       | 12.002      | -123.5      | 20.00005    | 1.01        |
+-------------+-------------+-------------+-------------+-------------+
| 10.01       | 12.002      | -123.5      | 20.00005    | 1.01        |
+-------------+-------------+-------------+-------------+-------------+
```
