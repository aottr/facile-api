# Request

| Method | Scope | Usage | Optional |
|----------|:---------------------|---------------|--------------|
| GET | Collection | Get all resources in a collection | `range` Parameter can be used for pagination. Range between two numbers requires a minus (`-`), otherwise it will be handled like a limit, starting from zero. |
| GET | Resource | Get a particular resource |  |
| POST | Collection | Create a new resource in a collection |  |
| PATCH | Resource | Update a resource | Null-values for fields that need to be reset. (comparison to PUT) |
| DELETE | Resource | Delete a resource |  |

```
PATCH /articles/2
{
	"body": "Heh. Bottom text."
}
```

```
GET /articles?range=100
```

```
GET /articles?range=50-99
```


## Go Further
- [Basics](basics.md)
- [Response](response.md)