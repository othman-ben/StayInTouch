<!-- The core Firebase JS SDK is always required and must be listed first -->

{% include firebase.html %}

{% include authentication.html %}

<script type="text/javascript">
      // FirebaseUI config.
      var uiConfig = {
        signInSuccessUrl: 'https://othman-ben.github.io/StayInTouch/business_info',
        signInOptions: [
          // Leave the lines as is for the providers you want to offer your users.
          firebase.auth.EmailAuthProvider.PROVIDER_ID
        ],

        // Terms of service url/callback.
        tosUrl: 'https://othman-ben.github.io/StayInTouch/TermsServices',
        // Privacy policy url/callback.
        privacyPolicyUrl: 'https://othman-ben.github.io/StayInTouch/PrivacyPolicy'
      };

      // Initialize the FirebaseUI Widget using Firebase.
      var ui = new firebaseui.auth.AuthUI(firebase.auth());

      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);
</script>

<div id="firebaseui-auth-container"></div>
