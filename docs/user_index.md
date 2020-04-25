<!-- JS -->
<script src="//ajax.googleapis.com/ajax/libs/angularjs/1.3.15/angular.min.js"></script>

{% include firebase.html %}
<script src="https://embed.typeform.com/embed.js" type="text/javascript"></script>

<script>
var app = angular.module('myApp', []);

$scope.checkLocalStorage = firebase.auth().onAuthStateChanged(function(user) {
  if (user) {
    return true
  } else {
    return false
  }
});
</script>

<script>
window.addEventListener("DOMContentLoaded", function() {
  var el = document.getElementById("my-embedded-typeform");

  // When instantiating a widget embed, you must provide the DOM element
  // that will contain your typeform, the URL of your typeform, and your
  // desired embed settings
  window.typeformEmbed.makeWidget(el, "https://benoitgufflet.typeform.com/to/lu4siV", {
    hideFooter: true,
    hideHeaders: true,
    opacity: 0
  });
});
</script>

<div ng-app="myApp" ng-if="checkLocalStorage()" id="my-embedded-typeform" style="width: 100%; height: 500px;"></div>

<div ng-app="myApp" ng-if="!checkLocalStorage()">
  Please login before being able to access the Private Citizen Interface.

  

  <button name="button" onclick="https://othman-ben.github.io/StayInTouch/user_login">User Login</button>

</div>
