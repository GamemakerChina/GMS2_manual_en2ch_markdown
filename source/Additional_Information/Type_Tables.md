# Type Tables

This page shows the all the different results that you may get when
using arithmetic on the different [data
types](../GameMaker_Language/GML_Overview/Data_Types) available. The
tables all follow the same format, with the columns showing the *left
hand* side of an arithmetical operation, and the rows showing the *right
hand* side, eg:

``` gml
&amp;lt;LHS&amp;gt; + &amp;lt;RHS&amp;gt; = &amp;lt;result&amp;gt;
```

|               |          |          |            |           |           |         |               |           |
|---------------|----------|----------|------------|-----------|-----------|---------|---------------|-----------|
|  Add (+)      | **Real** | **Bool** | **String** | **Int32** | **Int64** | **Ptr** | **undefined** | **Array** |
| **Real**      | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **Bool**      | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **String**    | String   | String   | String     | String    | String    |  Error  |  Error        |  Error    |
| **Int32**     | Real     | Real     |  Error     | Int32     | Int64     |  Error  |  Error        |  Error    |
| **Int64**     | Real     | Real     |  Error     | Int64     | Int64     |  Error  |  Error        |  Error    |
| **Ptr**       |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **undefined** |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Array**     |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |

|                |          |          |            |           |           |         |               |           |
|----------------|----------|----------|------------|-----------|-----------|---------|---------------|-----------|
|  Subtract (-)  | **Real** | **Bool** | **String** | **Int32** | **Int64** | **Ptr** | **undefined** | **Array** |
| **Real**       | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **Bool**       | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **String**     |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Int32**      | Real     | Real     |  Error     | Int32     | Int64     |  Error  |  Error        |  Error    |
| **Int64**      | Real     | Real     |  Error     | Int64     | Int64     |  Error  |  Error        |  Error    |
| **Ptr**        |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **undefined**  |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Array**      |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |

|                 |          |          |            |           |           |         |               |           |
|-----------------|----------|----------|------------|-----------|-----------|---------|---------------|-----------|
|  Multiply (\*)  | **Real** | **Bool** | **String** | **Int32** | **Int64** | **Ptr** | **undefined** | **Array** |
| **Real**        | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **Bool**        | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **String**      | String   |  Error   |  Error     | String    |  Error    |  Error  |  Error        |  Error    |
| **Int32**       | Real     | Real     |  Error     | Int32     | Int64     |  Error  |  Error        |  Error    |
| **Int64**       | Real     | Real     |  Error     | Int64     | Int64     |  Error  |  Error        |  Error    |
| **Ptr**         |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **undefined**   |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Array**       |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |

|               |          |          |            |           |           |         |               |           |
|---------------|----------|----------|------------|-----------|-----------|---------|---------------|-----------|
|  Divide (/)   | **Real** | **Bool** | **String** | **Int32** | **Int64** | **Ptr** | **undefined** | **Array** |
| **Real**      | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **Bool**      | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **String**    |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Int32**     | Real     | Real     |  Error     | Int32     | Int64     |  Error  |  Error        |  Error    |
| **Int64**     | Real     | Real     |  Error     | Int64     | Int64     |  Error  |  Error        |  Error    |
| **Ptr**       |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **undefined** |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Array**     |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |

|                |          |          |            |           |           |         |               |           |
|----------------|----------|----------|------------|-----------|-----------|---------|---------------|-----------|
|  Divide (div)  | **Real** | **Bool** | **String** | **Int32** | **Int64** | **Ptr** | **undefined** | **Array** |
| **Real**       | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **Bool**       | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **String**     |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Int32**      | Real     | Real     |  Error     | Int32     | Int64     |  Error  |  Error        |  Error    |
| **Int64**      | Real     | Real     |  Error     | Int64     | Int64     |  Error  |  Error        |  Error    |
| **Ptr**        |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **undefined**  |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Array**      |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |

|               |          |          |            |           |           |         |               |           |
|---------------|----------|----------|------------|-----------|-----------|---------|---------------|-----------|
|  Mod (%)      | **Real** | **Bool** | **String** | **Int32** | **Int64** | **Ptr** | **undefined** | **Array** |
| **Real**      | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **Bool**      | Real     | Real     |  Error     | Real      | Real      |  Error  |  Error        |  Error    |
| **String**    |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Int32**     | Real     | Real     |  Error     | Int32     | Int64     |  Error  |  Error        |  Error    |
| **Int64**     | Real     | Real     |  Error     | Int64     | Int64     |  Error  |  Error        |  Error    |
| **Ptr**       |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **undefined** |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |
| **Array**     |  Error   |  Error   |  Error     |  Error    |  Error    |  Error  |  Error        |  Error    |

## Equality Table

There are a few special constants that may or may not be equal to
themselves, as shown in the following table:

|                 |           |               |              |
|-----------------|-----------|---------------|--------------|
|  Equality (==)  | **NaN**   | **undefined** | **infinity** |
| **NaN**         | **false** | false         | false        |
| **undefined**   | false     | **true**      | false        |
| **infinity**    | false     | false         | **true**     |
