<script>
firebase.auth().onAuthStateChanged(function(user) {
  if (user) {
    {% include business.html %}
  } else {
    Please login before being able to access.
    <a href="https://othman-ben.github.io/StayInTouch/business_login" class="btn">Business Login</a>
  }
});
</script>


{% include firebase.html %}

{% include typeform.html url="" %}

{% include authentication.html %}

<div ng-app="myApp" ng-if="checkLocalStorage()" id="my-embedded-typeform" style="width: 100%; height: 500px;"></div>

<div ng-app="myApp" ng-if="!checkLocalStorage()">
  Please login before being able to access the Business Interface.



  <button name="button" onclick="https://othman-ben.github.io/StayInTouch/business_login">Business Login</button>

</div>

<script>
  const fs = require('fs')
  const customer = {
      name: "Newbie Co.",
      order_count: 0,
      address: "Po Box City",
  }
  const jsonString = JSON.stringify(customer)
  fs.writeFile('_data/businesses.json', jsonString, err => {
      if (err) {
          console.log('Error writing file', err)
      } else {
          console.log('Successfully wrote file')
      }
  })
</script>
