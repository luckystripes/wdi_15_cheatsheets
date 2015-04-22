Angular Cheatsheet

Angular Filters

custom filter:
create with
```myModule.filter('filterName', function(){
  return function(value) //factory-like setup returning a function that returns manipulated value.
    return //manipulate value here. 
});```


filtering input:
An input filter can be added to a directive with a pipe character (|) and filter followed by a colon and a model name.
e.g. 
```<p><input type="text" ng-model="test"></p>

<ul>
  <li ng-repeat="x in names | filter:test | orderBy:'country'">
    {{ (x.name | uppercase) + ', ' + x.country }}
  </li>
</ul>```


ng-click:
Separate expressions like so ```ng-click="sortField = 'name' ; reverse = !reverse"```


ng-model filter single field:
Passing an Object can filter specific properties
```filter: {name: 'john'}``` will filter all 'name's with value 'john'

Therefore   ```ng-repeat="user in users | filter:search"
                 ng-model: search['tel']                            //will filter by the field 'tel' only```