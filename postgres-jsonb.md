## Something on how to add a JSONB column

## Querying
`->` ???
`->>` as text
`?` check if a field is defined at all.

### Comparing values
Postgres sees the data mostly as text. Meaning that querying what is a JSON number, say 'id' in {"id": 1} is seen as text i.e. `SELECT '{"id": 1}'::jsonb->'id' = '1'` returns True

#### Null
`SELECT '{"name": null}'::jsonb->'name' IS NULL;` false because the db does infact have a value for you
`'{"name": null}::jsonb->>'name' IS NULL` is true as null in text is NULL.

#### Check if defined
`SELECT '{"name": null}'::jsonb ? 'age';` False

