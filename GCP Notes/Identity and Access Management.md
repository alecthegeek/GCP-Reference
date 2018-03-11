# Identify Access Management

[](https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2007_HandlingAuthenticationAuthorization.pdf)

# Cloud IAM Best Practice

- Least Priv
- Rotate Keys for service accounts and manage user account accounts
- Set IAM policies at org level
- Assign roles to groups in preference to accounts (service or user)
- Audit changes and maintain logging (Cloud Audit Logging)

# Service Accounts

- Belong to application or VM
- Used by application to call API or service
- have an email address
- and a key pair (max 10)
- can assign IAM roles to service accounts
- Keys can be created external to GCP — you are responsible for all key management

![Identify%20Access%20Management/Untitled.png](Identify%20Access%20Management/Untitled.png)

# OAuth 2.0

Allows an programme to access resources on behalf of a user.

IAP ⇒ Cloud Identity-Aware Proxy (IAP) via HTTPS

# Firebase Problem

    [8080-dot-11660086-dot-devshell.appspot.com](http://8080-dot-11660086-dot-devshell.appspot.com/)
    
    angular.js:15567 ReferenceError: firebase is not defined
    at angularfire.min.js:1
    at Object.authFactory (auth-factory.js:23)
    at Object.invoke (angular.js:5141)
    at Object.enforcedReturnValue [as $get] (angular.js:4976)
    at Object.invoke (angular.js:5141)
    at angular.js:4930
    at getService (angular.js:5084)
    at injectionArgs (angular.js:5109)
    at Object.invoke (angular.js:5133)
    at $controllerInit (angular.js:11704)
    
    <!DOCTYPE html>
    <!--
    Copyright 2017, Google, Inc.
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
    [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    -->
    <html>
    <head>
    <title>Quite Interesting Quiz</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' href='[//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css](notion://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css)'>
    </head>
    
    <body ng-app='qiqApp'>
    <nav class='navbar navbar-default'>
    <div class='container'>
    <div class='navbar-header'>
    <button type='button' class='navbar-toggle collapsed' ng-click='isNavCollapsed = !isNavCollapsed' aria-expanded='false'>
    <span class='sr-only'>Toggle navigation</span>
    <span class='icon-bar'></span>
    <span class='icon-bar'></span>
    <span class='icon-bar'></span>
    </button>
    <a class='navbar-brand' href='/'>Quite Interesting Quiz</a>
    </div>
    <div class='collapse navbar-collapse' uib-collapse='isNavCollapsed' id='bs-example-navbar-collapse-1'>
    <ul class='nav navbar-nav'>
    <li><a href='#!/quiz/gcp'>GCP</a></li>
    <li><a href='#!/quiz/places'>Places</a></li>
    <li><a href='#!/quiz/people'>People</a></li>
    </ul>
    <qiq-login></qiq-login>
    </div>
    </div>
    </nav>
    <div class='container'>
    <h1>Quite Interesting Quiz</h1>
    <div ng-view></div>
    </div>
    
        <!-- The core Firebase JS SDK is always required and must be listed first -->
        
    
    <script src="[https://www.gstatic.com/firebasejs/7.14.0/firebase-app.js](https://www.gstatic.com/firebasejs/7.14.0/firebase-app.js)"></script>
    
    <script src="[https://www.gstatic.com/firebasejs/7.5.0/firebase-auth.js](https://www.gstatic.com/firebasejs/7.5.0/firebase-auth.js)"></script>
    
    <script src="[https://www.gstatic.com/firebasejs/7.14.0/firebase-analytics.js](https://www.gstatic.com/firebasejs/7.14.0/firebase-analytics.js)"></script>
    
    <script>
    // Your web app's Firebase configuration
    var firebaseConfig = {
    apiKey: "AIzaSyDVOWDgnnWLKRejHCNFGi5vAJmVcaDsAtM",
    authDomain: "[qwiklabs-gcp-02-14ba309fd180.firebaseapp.com](http://qwiklabs-gcp-02-14ba309fd180.firebaseapp.com/)",
    databaseURL: "[https://qwiklabs-gcp-02-14ba309fd180.firebaseio.com](https://qwiklabs-gcp-02-14ba309fd180.firebaseio.com/)",
    projectId: "qwiklabs-gcp-02-14ba309fd180",
    storageBucket: "[qwiklabs-gcp-02-14ba309fd180.appspot.com](http://qwiklabs-gcp-02-14ba309fd180.appspot.com/)",
    messagingSenderId: "773540093938",
    appId: "1:773540093938:web:336633dad1b81763ac956b",
    measurementId: "G-GHRZWQN1EC"
    };
    // Initialize Firebase
    firebase.initializeApp(firebaseConfig);
    firebase.analytics();
    </script>
    
        <script src='//ajax.googleapis.com/ajax/libs/angularjs/1.7.8/angular.js'></script>
        <script src='//ajax.googleapis.com/ajax/libs/angularjs/1.7.8/angular-route.js'></script>
        <script src='//cdnjs.cloudflare.com/ajax/libs/angular-ui-bootstrap/2.5.0/ui-bootstrap-tpls.js'></script>
        <script src='<https://cdn.firebase.com/libs/angularfire/2.2.0/angularfire.min.js>'></script>
        
        <script src='app/app.js'></script>
        
        <script src='app/quizzes/quiz-module.js'></script>
        <script src='app/quizzes/quiz-factory.js'></script>
        <script src='app/quizzes/quiz-controller.js'></script>
        
        <script src='app/auth/auth-module.js'></script>
        <script src='app/auth/auth-factory.js'></script>
        <script src='app/auth/auth-controller.js'></script>
        <script src='app/auth/qiq-login.js'></script>
        
    
    </body>
    </html>