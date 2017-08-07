# Get basic information's of repository

Get the basic details of Bootstrap with stargazers count, watchers count, languages and etc,...

```
query {
  repository(owner:"twbs", name:"bootstrap") {
    createdAt
    pushedAt
    nameWithOwner
    description
    homepageUrl
    releases(last:1) {
      nodes {
        updatedAt
        name
      }
    }
    defaultBranchRef {
      name
    }
    issues(last:1, states:OPEN) {
      totalCount
    }
    primaryLanguage {
      name
      color
    }
    languages(last:100) {
      totalSize
      edges {
        size
        node {
          name
          color
          id
        }
      }
    }
    owner {
      avatarUrl
    }
    stargazers {
      totalCount
    }
    watchers {
      totalCount
    }
  }
}
```

Responsed of Github:

```
{
  "data": {
    "repository": {
      "createdAt": "2011-07-29T21:19:00Z",
      "pushedAt": "2017-08-07T05:56:24Z",
      "nameWithOwner": "twbs/bootstrap",
      "description": "The most popular HTML, CSS, and JavaScript framework for developing responsive, mobile first projects on the web.",
      "homepageUrl": "http://getbootstrap.com",
      "releases": {
        "nodes": [
          {
            "updatedAt": "2017-01-06T17:45:52Z",
            "name": "v4.0.0-alpha.6"
          }
        ]
      },
      "defaultBranchRef": {
        "name": "v4-dev"
      },
      "issues": {
        "totalCount": 190
      },
      "primaryLanguage": {
        "name": "JavaScript",
        "color": "#f1e05a"
      },
      "languages": {
        "totalSize": 890974,
        "edges": [
          {
            "size": 425736,
            "node": {
              "name": "JavaScript",
              "color": "#f1e05a",
              "id": "MDg6TGFuZ3VhZ2UxNDA="
            }
          },
          {
            "size": 110395,
            "node": {
              "name": "HTML",
              "color": "#e34c26",
              "id": "MDg6TGFuZ3VhZ2U0MTc="
            }
          },
          {
            "size": 344504,
            "node": {
              "name": "CSS",
              "color": "#563d7c",
              "id": "MDg6TGFuZ3VhZ2UzMDg="
            }
          },
          {
            "size": 935,
            "node": {
              "name": "PowerShell",
              "color": "#012456",
              "id": "MDg6TGFuZ3VhZ2UyNjQ="
            }
          },
          {
            "size": 7835,
            "node": {
              "name": "Ruby",
              "color": "#701516",
              "id": "MDg6TGFuZ3VhZ2UxNDE="
            }
          },
          {
            "size": 1569,
            "node": {
              "name": "Shell",
              "color": "#89e051",
              "id": "MDg6TGFuZ3VhZ2UxMzk="
            }
          }
        ]
      },
      "owner": {
        "avatarUrl": "https://avatars0.githubusercontent.com/u/2918581?v=4"
      },
      "stargazers": {
        "totalCount": 113497
      },
      "watchers": {
        "totalCount": 7046
      }
    }
  }
}
```
