### PROBLEM: TEMPLATES

```html
[ <a href="" ng-click="todoList.archive()">archive</a> ]
<ul class="unstyled">
  <li ng-repeat="todo in todoList.todos">
    <label class="checkbox">
      <input type="checkbox" ng-model="todo.done">
      <span class="done-{{todo.done}}">{{todo.text}}</span>
    </label>
  </li>
</ul>
```
```JavaScript
angular.module('todoApp', [])
  .controller('TodoListController', function() {
    var todoList = this;
    todoList.todos = [
      {text:'learn angular', done:true},
      {text:'build an angular app', done:false}];

    todoList.archive = function() {
      var oldTodos = todoList.todos;
      todoList.todos = [];
      angular.forEach(oldTodos, function(todo) {
        if (!todo.done) todoList.todos.push(todo);
      });
    };
  });
```
