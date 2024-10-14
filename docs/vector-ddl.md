# Vector DDL

```sql
vector -- Equivalent to vector(2000)

vector(512) -- 512-dimensional vector of float32

vector(float64, 128) -- 128-dimensional vector of float64
```

## BNF

```bnf
<declaration> ::= "vector" [ "(" [ <vector_type> "," ] <dim> ")" ]
<vector_type> ::= "float32" | "float64"
<dim> ::= <positive_integer>
<positive_integer> ::= {digit}+
```

## Examples

### Create table

```sql
CREATE TABLE items (
  host_year INT NOT NULL PRIMARY KEY,
  embedding vector(3)
);
```

### Create Column

```sql
ALTER TABLE items
ADD COLUMN embedding vector(3);
```
