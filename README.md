
# Quines

## PostgreSQL

A PostgreSQL quine adapted from this [ANSI SQL quine](https://archive.wikiwix.com/cache/index2.php?url=http%3A%2F%2Fsgbd.arbinada.com%2Fnode%2F33#federation=archive.wikiwix.com) (works for *PostgreSQL 11.15*):

```sql
SELECT left(A.v, 81) || chr(39) || A.v || chr(39) || right(A.v, 12) FROM (SELECT 'SELECT left(A.v, 81) || chr(39) || A.v || chr(39) || right(A.v, 12) FROM (SELECT AS v) AS A;' AS v) AS A;
```

