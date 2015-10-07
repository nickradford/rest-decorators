# rest-decorators

ES7 decorators for describing restful interfaces. Uses `window.fetch` under the hood to make ajax requests

## Example

```js
class User {
  
  @get
  @path('/api/users/:id')
  @params(':id')
  static findOne(user) {
    // Do any data transformation
    return user
  }
  
}

User.findOne('1234').then(function(user) {
  app.selectedUser = user
})
```

### API

#### @get
#### @post
#### @put
#### @delete

#### @path(string)
#### @params(args)
