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
