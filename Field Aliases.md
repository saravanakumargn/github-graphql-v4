# Field Aliases

Find both open issues and closed issues using Field Aliases in Github GraphQL v4

Github GraphQL query to find the open and closed issues of Bootstrap using Field Aliases.

```
query {
  repository(owner: "twbs", name: "bootstrap") {
    nameWithOwner
    description
    homepageUrl
    pushedAt
    closedIssues: issues(last: 1, states: CLOSED) {
      closedIssuesCount: totalCount
    }
    openIssues: issues(last: 1, states: OPEN) {
      openIssuesCount: totalCount
    }
  }
}
```
Server responded JSON data:

```
{
  "data": {
    "repository": {
      "nameWithOwner": "twbs/bootstrap",
      "description": "The most popular HTML, CSS, and JavaScript framework for developing responsive, mobile first projects on the web.",
      "homepageUrl": "http://getbootstrap.com",
      "pushedAt": "2017-08-07T05:56:24Z",
      "closedIssues": {
        "closedIssuesCount": 15090
      },
      "openIssues": {
        "openIssuesCount": 190
      }
    }
  }
}
```
