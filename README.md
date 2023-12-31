
# Exercise tracker


Project created to learn nodeJS

Project was based on this task from freeCodeCamp
https://www.freecodecamp.org/learn/back-end-development-and-apis/back-end-development-and-apis-projects/exercise-tracker 


## API Reference

### Create new user

```http
  POST  /api/users 
```

| Body object  | Type     | Description                |
| :--------- | :------- | :------------------------- |
| `username` | `string` | **Required** |

### Get all users

```http
  GET /api/users 
```

### Create new exercise for user
```http
  POST  /api/users/:_id/exercises 
```

| Parameter  | Type     | Description                |
| :--------- | :------- | :------------------------- |
| `_id `     | `string` | **Required** user id|

Return data, array of:
| user object []  | Type     
| :---------      | :------- 
| `username `     | `string` 
| `_id `          | `string` 

Body:
| exercise object  | Type     
| :---------       | :------- 
| `username `      | `string` 
| `description `   | `string` 
| `duration `      | `number` 
| `date `          | `string`
| `_id `           | `string` 


### Get logs for user exercises
```http
  get  /api/users/:_id/logs
```

| Parameter  | Type     | Description                |
| :--------- | :------- | :------------------------- |
| `_id `     | `string` | **Required** user id|


Return data:
| object   | Type     
| :---------   | :------- 
| `username `  | `string` 
| `count `     | `number` 
| `_id `       | `string` 
| `log `       | `log object` 


| log object      | Type     
| :---------      | :------- 
| `description `  | `string` 
| `duration `     | `number` 
| `date `         | `string` 
