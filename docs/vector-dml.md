# Vector Types

## BNF

```bnf
<declaration> ::= "vector" [ "(" [ <vector_type> "," ] <dim> ")" ]
<vector_type> ::= "float32" | "float64"
<dim> ::= <positive_integer>
<positive_integer> ::= {digit}+
```

## Examples

```sql
vector -- Equivalent to vector(2000)

vector(512) -- 512-dimensional vector of float32

vector(float64, 128) -- 128-dimensional vector of float64
```
