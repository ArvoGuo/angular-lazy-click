lazy-click
==========

### 描述

按钮执行点击事件后，默认2s内点击操作失效，并在2s内添加disabled类， 2s后恢复初始状态

#### install

npm i angular-lazy-click --save

or

bower i angular-lazy-click --save

#### demo

```js

angular.module('[your module]', ['angular-lazy-click'])

angular.controller('test', function($scope) {
  $scope.test1 = function() {
    console.log(1);
  }

  $scope.test2 = function(string) {
    console.log(string);
  }
});

```

```html
<!-- 初始状态 -->
<div class="" lazy-click="test1();test2('string');">Test</div>

<!-- 点击后两秒内 ， 点击无效 -->
<div class="disabled" lazy-click="test1();test2('string');">Test</div>

<!-- 点击后两秒后 -->
<div class="" lazy-click="test1();test2('string');">Test</div>
```

#### 属性

`lazy-click`, 与ng-click用法一致

`lazy-click-time`, 点击失效时间，默认为2s，允许不设置，格式： lazy-click-time="3000"
