# addStar

This mutation is help to add the star.

### Basic structure

```
mutation {
  addStar(input:{clientMutationId:"<<insert user id here>>", starrableId:"<<insert repostory id>>"}) {
    starrable {
      id
    }
  }
}
```

This is the respose which contains new created star id.

```
{
  "data": {
    "addStar": {
      "starrable": {
        "id": "<<new created id>>"
      }
    }
  }
}
```

