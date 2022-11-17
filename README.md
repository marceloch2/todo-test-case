# Todo App - Test Driven RESTful JSON API

JSON API with a full set of RESTful endpoints:

| RESTful Route         | Description              | controller#action |
| :-------------------- | :----------------------- | :---------------- |
| `POST` `/todos`       | Create a new todo record | create            |
| `GET` `/todos`        | Fetch a list of todos    | index             |
| `GET` `/todos/10`     | Fetch one specific todo  | show              |
| `PUT` `/todos/11`     | Change one specific todo | update            |
| `DELETE` `/todos/11`  | Remove one specific todo | destroy           |
| `GET` `/todos/search` | **Bonus**: Search todos  | search            |

Example of the Test that could be made for those endpoints

    Todos API
       GET /api/todos (index)
         ✓ should respond with status 200
         ✓ should respond with a JSON object
         ✓ the JSON should have a key "todos" that points to a list (value) of todos
         ✓ todo objects should have properities: _id, description, task
       GET /api/todos/:id (show)
         ✓ should respond with status 200 - Success
         ✓ should respond with JSON
         ✓ should fetch one specific todo by _id
       POST /api/todos (create)
         ✓ should respond with status 200 - Success
         ✓ should respond with JSON
         ✓ should respond with the new todo object
         ✓ should assign an _id to the new todo object
         ✓ should increment the _id number by one each time a todo is created
       DELETE /api/todos/:id (destroy)
         ✓ should respond with 200 or 204 on success
         ✓ should delete one specific todo from the list of todos
       PUT /api/todos/:id (update)
         ✓ should respond with status 200 - Success
         ✓ should respond with JSON
         ✓ should update the properties of one specific todo
       GET /api/todos/search (search)
         ✓ should list all todos that contain the search term from the query parameter (e.g. `?q=discover`) in the task field

## Bonuses

1. Build a way for a user to search for todos.
2. Build an Interface.
