### Retrieve TODO List

#####Request
`GET /api/todos/v1.0.1/14 HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK

{
"todos" : [
   { 
     "id": "1228",
     "name" : "Get Milk",
     "description": "remember to get milk for cake",
     "category": "shopping",
     "owner": "Kai"
   }
 ]
}

```

### Add a new TODO item

#####Request
```
POST /api/todos/v1.0.1/ HTTP/1.1

{ 
  "name" : "Buy cheese",
  "description": "remember to buy cheese from the shop",
  "category": "shopping",
  "owner": "Kai"
}

```

#####Response
```
HTTP/1.1 201 Created

{ 
  "id" : "20089",
  "name" : "Buy cheese",
  "description": "remember to buy cheese from the shop",
  "category": "shopping",
  "owner": "Kai"
}
```
