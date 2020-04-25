<!-- The core Firebase JS SDK is always required and must be listed first -->
<script src="https://www.gstatic.com/firebasejs/7.14.2/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/7.14.2/firebase-auth.js"></script>

<script>
var firebaseConfig = {
apiKey: "AIzaSyDy_NDLhK4_wnUpP7_x4w9Q4cBLjTJINac",
authDomain: "stayintouch-1fd88.firebaseapp.com",
databaseURL: "https://stayintouch-1fd88.firebaseio.com",
projectId: "stayintouch-1fd88",
storageBucket: "stayintouch-1fd88.appspot.com",
messagingSenderId: "699177114486",
appId: "1:699177114486:web:ff3d62b93a7012b4743857"
};

// Initialize Firebase
firebase.initializeApp(firebaseConfig);
</script>

<script src="https://www.gstatic.com/firebasejs/ui/4.5.0/firebase-ui-auth__en.js"></script>
<link type="text/css" rel="stylesheet" href="https://www.gstatic.com/firebasejs/ui/4.5.0/firebase-ui-auth.css" />
<script type="text/javascript">
      // FirebaseUI config.
      var uiConfig = {
        signInSuccessUrl: 'https://othman-ben.github.io/StayInTouch/user_index',
        signInOptions: [
          firebase.auth.PhoneAuthProvider.PROVIDER_ID
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
      var ui = new firebaseui.auth.AuthUI(firebase.auth());
      // The start method will wait until the DOM is loaded.
      ui.start('#firebaseui-auth-container', uiConfig);

      window.recaptchaVerifier = new firebase.auth.RecaptchaVerifier('sign-in-button', {
        'size': 'invisible',
        'callback': function(response) {
          // reCAPTCHA solved, allow signInWithPhoneNumber.
          onSignInSubmit();
        }
      });
</script>

<div id="firebaseui-auth-container"></div>
