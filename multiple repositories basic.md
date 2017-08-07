
# multiple repositories basic


```
query {
  bootstrap: repository(owner:"twbs", name:"bootstrap") {
    pushedAt
    nameWithOwner
    homepageUrl
    primaryLanguage {
      name
      color
    }
  }
  purecss: repository(owner:"yahoo", name:"pure") {
    pushedAt
    nameWithOwner
    homepageUrl
    owner {
      avatarUrl
    }
    stargazers {
      totalCount
    }
  }
}
```

Github server JSON response:

```
{
  "data": {
    "bootstrap": {
      "pushedAt": "2017-08-07T05:56:24Z",
      "nameWithOwner": "twbs/bootstrap",
      "homepageUrl": "http://getbootstrap.com",
      "primaryLanguage": {
        "name": "JavaScript",
        "color": "#f1e05a"
      }
    },
    "purecss": {
      "pushedAt": "2017-08-01T18:14:20Z",
      "nameWithOwner": "yahoo/pure",
      "homepageUrl": "http://purecss.io/",
      "owner": {
        "avatarUrl": "https://avatars1.githubusercontent.com/u/16574?v=4"
      },
      "stargazers": {
        "totalCount": 17271
      }
    }
  }
}
```
