{% include firebase.html %}

{% include authentication.html %}

<div ng-app="myApp" ng-if="checkLocalStorage()">
Welcome to your Business Owner space!

This is where you will be able to access the QR code to put in front of your store, to access some governmental material to share with your clients, the alerts that you will receive from clients, and the possibility to alert clients if one of your employees becomes sick.

</div>

<div ng-app="myApp" ng-if="!checkLocalStorage()">
  Please login before being able to access the Private Citizen Interface.



  <button name="button" onclick="https://othman-ben.github.io/StayInTouch/user_login">User Login</button>

</div>
