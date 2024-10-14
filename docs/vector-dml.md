# Vector DML

This page describes CRUD operations on vectors.

## Create and insert vector into a table

```sql
INSERT INTO items (
  embedding
)
VALUES
  ('[1,2,3]'),
  ('[4,5,6]');
```

## Read vectors

```sql
SELECT *
FROM items
LIMIT 5;
```

### Read nearest neighbor vectors (Exact)

By using vector distance operators

```sql
SELECT * FROM items
ORDER BY embedding <-> '[3,1,2]'
LIMIT 5;
```

Or, by using vector distance functions

```sql
SELECT * FROM items
ORDER BY l2_distance(embedding, '[3, 1, 2]')
LIMIT 5;
```

The above two statements are equivalent.

### Read vector with vector index (Approximate)

## Update vector

## Delete vector
