---
description: 'https://www.elastic.co/start'
---

# ElasticSearch

SQL is very limited. See: [https://www.elastic.co/guide/en/elasticsearch/reference/current/sql-syntax-select.html](https://www.elastic.co/guide/en/elasticsearch/reference/current/sql-syntax-select.html) Examples:

```text
SELECT title FROM "en-wikipedia" WHERE MATCH(title, 'interesting') LIMIT 100;

SELECT revision.text._ as text FROM "en-wikipedia" WHERE title = 'May you live in interesting times' LIMIT 1;

SELECT title, revision.text._ as text FROM "en-wikipedia" WHERE MATCH(text, 'interesting') LIMIT 10;

SELECT score, title FROM (SELECT SCORE() as score, title, revision.text._ as text FROM "en-wikipedia" WHERE MATCH(text, 'interesting') ORDER BY score DESC LIMIT 100);
```

EQL reference, for use with Javascript or other Object-based queries:  
[https://www.elastic.co/guide/en/elasticsearch/client/javascript-api/current/api-reference.html](https://www.elastic.co/guide/en/elasticsearch/client/javascript-api/current/api-reference.html)

Full text search reference: [https://www.elastic.co/guide/en/elasticsearch/reference/current/full-text-queries.html](https://www.elastic.co/guide/en/elasticsearch/reference/current/full-text-queries.html)

## Javascript SDK:

[https://github.com/elastic/elasticsearch-js](https://github.com/elastic/elasticsearch-js)

```text
import { Client } from "@elastic/elasticsearch"
const client = new Client({ node: "http://localhost:9200" })

// promise API
const result = await client.search({
  index: "en-wikipedia",
  body: {
    query: {
      match: { title: "tiger king" }
    }
  }
})
```

**Tutorial: Use with Node JS**  
[https://ciphertrick.com/elasticsearch-and-nodejs-tutorial/](https://ciphertrick.com/elasticsearch-and-nodejs-tutorial/) 

