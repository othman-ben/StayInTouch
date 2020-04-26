{% include typeform.html %}

<div ng-app="myApp" ng-if="checkLocalStorage()" id="my-embedded-typeform" style="width: 100%; height: 500px;"></div>

<div ng-app="myApp" ng-if="!checkLocalStorage()">
  Please login before being able to access the Business Interface.



  <button name="button" onclick="https://othman-ben.github.io/StayInTouch/business_login">Business Login</button>

</div>
