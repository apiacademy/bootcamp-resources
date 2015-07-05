### Retrieve the TODO List

#####Request
`GET /api/todos/ HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/json"

{
"todos" : [
   { 
     "id": "1228",
     "name" : "Get Milk",
   },
   { 
     "id": "1241",
     "name" : "Make Cake",
   }
 ]
}

```

### Retrieve a TODO item
#####Request
`GET /api/todos/14 HTTP/1.1`

#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/json"

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
POST /api/todos/ HTTP/1.1

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
Content-Type: "application/json"

{ 
  "id" : "20089",
  "name" : "Buy cheese",
  "description": "remember to buy cheese from the shop",
  "category": "shopping",
  "owner": "Kai"
}
```


### Remove a TODO item
#####Request
```
DELETE /api/todos/{id} HTTP/1.1
```
#####Response
```
HTTP/1.1 204 No Content
```

### Replace a TODO item
#####Request
```
PUT /aip/todos/{id} HTTP/1.1
{ 
  "name" : "Buy cheese",
  "description": "remember to buy cheese from the shop",
  "category": "shopping",
  "owner": "Kai"
}
```
#####Response
```
HTTP/1.1 200 OK
Content-Type: "application/json"

{ 
  "id" : "20089"
  "name" : "Buy cheese",
  "description": "remember to buy cheese from the shop",
  "category": "shopping",
  "owner": "Kai"
}
```
