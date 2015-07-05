### Home Page

#####Request
`GET /api/todos/ HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/hal+json"

{
    "_links": {
        "self": { "href": "/api/todos" },
        "curies": [{ "name": "todo", "href": "http://api.com/docs/rels/{rel}", "templated": true }],
        "todo:list": {
            "href": "/api/todos/list"
        },
        "todo:get-item": {
            "href": "/api/todos/item/{id}",
            "templated": "true",
            "title": "Todo Item"
        }
    }
}
```

### List Todos

#####Request
`GET /api/todos/list HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/json"

HTTP/1.1 200 OK
Content-Type: "application/hal+json"

{
    "_links": {
        "self": { "href": "/api/todos/list" },
        "curies": [{ "name": "todo", "href": "http://api.com/docs/rels/{rel}", "templated": true }],
        "next": { "href": "/api/todos/list?start=2" }
        "all" : { "href": "/api/todos/list?all" }
        "todo:get-item": {
            "href": "/api/todos/item/{id}",
            "templated": "true",
            "title": "Todo Item"
        }
    },
    "todos" : [
      { 
        "_links": {
         "self": { "href": "/api/todos/item/1228" },
        },
        "name" : "Get Milk",
        "description": "remember to get milk for cake",
        "category": "shopping",
        "owner": "Kai"
      }
   ]
}
```

### Retrieve a TODO item
#####Request
`GET /api/todos/1228 HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/json"

{
   "_links": {
      "self": { "href": "/api/todos/item/1228" },
      "curies": [{ "name": "todo", "href": "http://api.com/docs/rels/{rel}", "templated": true }],
      "todo:list": {
         "href": "/api/todos/list",
         "title": "Todo Item"
      }
   },
   "name" : "Get Milk",
   "description": "remember to get milk for cake",
   "category": "shopping",
   "owner": "Kai"
}
```

