<!-- JS -->
<script src="//ajax.googleapis.com/ajax/libs/angularjs/1.3.15/angular.min.js"></script>

{% include firebase.html %}
<script src="https://embed.typeform.com/embed.js" type="text/javascript"></script>

<script>
firebase.auth().onAuthStateChanged(function(user) {
  if (user) {
    this.logged=True
  } else {
    this.logged=False
  }
});
</script>

<script>
window.addEventListener("DOMContentLoaded", function() {
  var el = document.getElementById("my-embedded-typeform");

  // When instantiating a widget embed, you must provide the DOM element
  // that will contain your typeform, the URL of your typeform, and your
  // desired embed settings
  window.typeformEmbed.makeWidget(el, "https://admin.typeform.com/lu4siV", {
    hideFooter: true,
    hideHeaders: true,
    opacity: 0
  });
});
</script>

<div id="my-embedded-typeform" style="width: 100%; height: 300px;"></div>

<div *ngIf="logged; else #isAnonymous" id="my-embedded-typeform" style="width: 100%; height: 300px;">
</div>

<ng-template #isAnonymous>
  Please login before being able to access the Private Citizen Interface.

  <a href="https://othman-ben.github.io/StayInTouch/user_login" class="btn">User Login</a>

</ng-template>
