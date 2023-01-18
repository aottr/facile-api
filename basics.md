# Basic specification

## Path building
- Each endpoint represents a ressource and is **plural**
```
/users
/boxes
/books
/pets
```
- Paths should have a dynamic definition to address individual data. It is valid to use different variable identifiers if they are disjunct / cover-free. This can be reached by plain number / character identifiers or regular expressions in the logic. Although it is valid, it should be avoided for easability.
```
/users/1
/users/alex
/pets/332
/pets/ardoise
```
- Paths can also have a concrete definition
```
/pets/mine
/users/me
```
- If the call of a certain path is supposed to execute an action, this can be implemented as an *Action*. Actions may be at root-level or after identifying individual ressources and need to be a `POST`-Request. 
```
POST

/users/34/activate
```

## Go Further
- [Response](response.md)
- [Request](request.md)