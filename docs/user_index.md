{% include firebase.html %}

<script>
firebase.auth().onAuthStateChanged(function(user) {
  if (user) {
    {% include user.html %}
  } else {
    Please login before being able to access.
    <a href="https://othman-ben.github.io/StayInTouch/user_login" class="btn">User Login</a>
  }
});
</script>
