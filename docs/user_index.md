{% include firebase.html %}

{% include authentication.html %}

<div ng-app="myApp" ng-if="checkLocalStorage()">
Welcome to your Private Citizen space!

This is where you will be able to access your user information (history of businesses you have been to in the past 3 weeks) as well as alert all of these businesses if you ever become infected.

</div>

<div ng-app="myApp" ng-if="!checkLocalStorage()">
  Please login before being able to access the Private Citizen Interface.



  <button name="button" onclick="https://othman-ben.github.io/StayInTouch/user_login">Private Citizen Login</button>

</div>
