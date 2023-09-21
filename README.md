# 8
 Follow the simple step-by-step instructions, and watch as the ingredients transform into a delectable masterpiece that will tantalize your taste buds and leave you craving for more. Perfect for gatherings, family meals, or a cozy night in, this recipe is bound to become a favorite in your repertoire."
<html>
<head>
<h2> Simple Calculator using AngularJS</h2>
</head>
<script src= "https://ajax.googleapis.com/ajax/libs/angularjs/1.3.14/angular.min.js">
</script>
<style>
body{font: 12px/20px 'Lucida Grande' Tahoma, Verdana, sans-serif;
  color: red;
  text-align: center;
}
</style>
<script>
angular.module('CalculatorApp', []).controller('CalculatorController', function($scope) {
        $scope.result = function() {
            if ($scope.operator == '+') {
                return $scope.a + $scope.b;
            }
            if ($scope.operator == '-') {
                return $scope.a - $scope.b;
            }
            if ($scope.operator == '*') {
                return $scope.a * $scope.b;
            }
            if ($scope.operator == '/') {
                return $scope.a / $scope.b;
            }
        };
    });
</script>
<body>
<div ng-app="CalculatorApp" ng-controller="CalculatorController">
  <p><input type="number" ng-model="a"></p>
  <p><input type="number" ng-model="b"></p>
  <p><select ng-model="operator">
        <option>+</option>
        <option>*</option>
        <option>-</option>
        <option>/</option>
     </select></p>
  <p>Result: {{ result() }}</p>
 </div>
</body></html>

