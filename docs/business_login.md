<!-- The core Firebase JS SDK is always required and must be listed first -->

{% include firebase.html %}

<link type="text/css" rel="stylesheet" href="https://www.gstatic.com/firebasejs/ui/4.5.0/firebase-ui-auth.css" />
<script type="text/javascript">
      // FirebaseUI config.
      var uiConfig = {
        signInSuccessUrl: 'https://othman-ben.github.io/StayInTouch/business_index',
        signInOptions: [
          // Leave the lines as is for the providers you want to offer your users.
          firebase.auth.EmailAuthProvider.PROVIDER_ID
        ],
        // tosUrl and privacyPolicyUrl accept either url string or a callback
        // function.
        // Terms of service url/callback.
        tosUrl: 'https://othman-ben.github.io/StayInTouch/TermsServices',
        // Privacy policy url/callback.
        privacyPolicyUrl: function() {
          window.location.assign('https://othman-ben.github.io/StayInTouch/PrivacyPolicy');
        }
      };

      // Initialize the FirebaseUI Widget using Firebase.
      var ui = new firebaseui.auth.AuthUI(firebase.auth().setPersistence(firebase.auth.Auth.Persistence.LOCAL));
      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);$
</script>

<div id="firebaseui-auth-container"></div>
