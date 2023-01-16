# Response

Following this specification it is expected to have (at least) two keys at root-level
Having the `data` key is necessary since some applications can't handle root-level arrays as response.

```
GET /articles
{
    status: "success",
    data: {
        "post": { "id": 1, "title": "A blog post", "body": "Some useful content" }
     }
}
```

| Type | Description | Required Keys | Optional Keys |
|----------|:---------------------|---------------:|--------------:|
| success | Execution was successful | status, data | |
| failure | E.g. Client Errors appeared during execution | status, message | data |
| error | Server Errors appeared, e.g. due to a migration | status, message | data |

### Further examples

```
GET /boxes/2
{
    status: "failure",
    message: "Did not find the requested ressource."
    data: { 
	    param: {
		    "id": 2 
	    }
    }
}
```

```
POST /articles
{
	"status": "error".
	"message": "The backendservice was not reachable.",
	"data": {
		"title": "Just another blog article",
		"body": "Bottom text. heh."
	}
}
```

## Go Further
- [Basics](basics.md)
- [Request](request.md)