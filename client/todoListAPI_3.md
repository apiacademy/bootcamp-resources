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
        "prompt" : "Enter search string",
        "data" :
        [
          {"name" : "search", "value" : ""}
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
        "prompt" : "Enter search string",
        "data" :
        [
          {"name" : "search", "value" : ""}
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
