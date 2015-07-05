#Overview
This API uses the Collection+JSON media type.  It supports listing todo items, searching for a todo item and creating, reading, updating and deleting individual items.  
Consult https://github.com/collection-json/spec for details on the implicit CRUD behaviour for Collection+JSON items.
### TODO List Collection

#####Request
`GET /api/todos HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/vnd.collection+json"

{
  "collection" :
  {
    "version" : "1.0",
    "href" : "/api/todos",
    "items" : [
      {
        "href" : "/api/todos/items/1448",
        "data" : [
          {"prompt": "Todo", "name" : "title", "value": "Get milk"},
          {"prompt": "Description", "name" : "description", "value": "Buy milk for cake."},
          {"prompt": "Category", "name" : "category", "value": "Shopping"}
        ],
        "links" : [
          {"rel" : "owner", "href" : "/api/todos/users/rmitra", "prompt" : "Owner"}
        ]
      }
    ],
    "queries" : [
      {
        "href" : "/search",
        "rel" : "search",
        "prompt" : "Enter search string using Lucene query language",
        "data" :
        [
          {"name" : "name-search", "value" : ""}
        ]
      }
    ],
    "template" : {
      "data" : [
        {"name" : "title", "value" : "", "prompt" : "Todo Title"},
        {"name" : "description", "value" : "", "prompt" : "Description"},
        {"name" : "category", "value" : "", "prompt" : "Category"}
      ]
    }
}

```

### TODO List Item
#####Request
`GET /api/todos/items/14 HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/vnd.collection+json"

{
  "collection" :
  {
    "version" : "1.0",
    "href" : "/api/todos/items/14",
    "links" : [
      {"rel" : "collection", "href" : "/api/todos"}
    ],
    "items" : [
      {
        "href" : "/api/todos/items/14",
        "data" : [
          {"prompt": "Todo", "name" : "title", "value": "Get milk"},
          {"prompt": "Description", "name" : "description", "value": "Buy milk for cake."},
          {"prompt": "Category", "name" : "category", "value": "Shopping"}
        ],
        "links" : [
          {"rel" : "owner", "href" : "/api/todos/users/rmitra", "prompt" : "Owner"}
        ]
      }
    ],
    "queries" : [
      {
        "href" : "/search",
        "rel" : "search",
        "prompt" : "Enter search string using Lucene query language",
        "data" :
        [
          {"name" : "name-search", "value" : ""}
        ]
      }
    ],
    "template" : {
      "data" : [
        {"name" : "title", "value" : "", "prompt" : "Todo Title"},
        {"name" : "description", "value" : "", "prompt" : "Description"},
        {"name" : "category", "value" : "", "prompt" : "Category"}
      ]
    },
    
}

```
