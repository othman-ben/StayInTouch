{% include firebase.html %}

{% include typeform.html url="https://benoitgufflet.typeform.com/to/lu4siV" %}

{% include authentication.html %}

<div ng-app="myApp" ng-if="checkLocalStorage()" id="my-embedded-typeform" style="width: 100%; height: 500px;"></div>

<div ng-app="myApp" ng-if="!checkLocalStorage()">
  Please login before being able to access the Private Citizen Interface.



  <button name="button" onclick="https://othman-ben.github.io/StayInTouch/user_login">User Login</button>

</div>
