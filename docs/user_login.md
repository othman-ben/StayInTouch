<!-- The core Firebase JS SDK is always required and must be listed first -->

{% include firebase.html %}

<script type="text/javascript">

      // FirebaseUI config.
      var uiConfig = {
        signInSuccessUrl: 'https://othman-ben.github.io/StayInTouch/user_index',
        signInOptions: [{
          provider: firebase.auth.PhoneAuthProvider.PROVIDER_ID,
          recaptchaParameters: {
            type: 'image',
            size: 'invisible',
            badge: 'inline'
          },
          defaultCountry: 'FR'
        }
        ],

        // Terms of service url
        tosUrl: 'https://othman-ben.github.io/StayInTouch/TermsServices',

        // Privacy policy url
        privacyPolicyUrl: 'https://othman-ben.github.io/StayInTouch/PrivacyPolicy'
      };

      // Initialize the FirebaseUI Widget using Firebase.
      var ui = new firebaseui.auth.AuthUI(firebase.auth());
      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);
</script>

<div id="firebaseui-auth-container"></div>
