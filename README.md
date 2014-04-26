# BizRez Worklist Assignments

# curl

## CRUD(l)

Cookie based session - unfortunately each time you switch to a directory '/name' you have to pass in a users credentials

- curl -H "Content-Type: application/json" -b cookies.txt -c cookies.txt -X GET -d '{"name":"john","password":"password"}' http://localhost:3000/authenticate
- curl -H "Content-Type: application/json" -b cookies.txt -c cookies.txt -X POST -d '{"name":"john","password":"password"}' http://localhost:3000/assignments/create
- curl -H "Content-Type: application/json" -b cookies.txt -c cookies.txt -X GET -d '{"name":"john","password":"password"}' http://localhost:3000/assignments/read
- curl -H "Content-Type: application/json" -b cookies.txt -c cookies.txt -X POST -d '{"name":"john","password":"password"}' http://localhost:3000/assignments/update
- curl -H "Content-Type: application/json" -b cookies.txt -c cookies.txt -X DELETE -d '{"name":"john","password":"password"}' http://localhost:3000/assignments/delete
- curl -H "Content-Type: application/json" -b cookies.txt -c cookies.txt -X GET -d '{"name":"john","password":"password"}' http://localhost:3000/assignments/list





# JSON
## Required Properties

```
assignee = {
  orgUnit: 'Organization unit',
  ownerId: 'owner of assignment',
  ownerType: 'person || system'
}

assignment = {
  assignee: {Object of type assignee},
  type: 'type of assignment'
  status: 'new, open, closed, hold',
  statusInfo: 'why, what, where',
  priority: 'low, med, high',
  goalDate: Date(),
  deadlineDate Date(),
  header: '{} Object header',
  body: '{} Object of details',
  sourcelink: 'link to source for deep linking',
  id: 'system generated'
}

```

#

### list


