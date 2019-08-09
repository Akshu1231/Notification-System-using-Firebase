# Notification-System-using-Firebase
This is a simple project for subscribing and sending notfication for a web application . This project uses Firebase to store tokens of users for every subscription. Whenever It detect some change in database or if you want to send some notification to the subscribers , It pushes the notification to all the users using FCM with the help of tokens.

#Setting Up Firebase to Your Project =>

##Creating a simple project :

-> npm init

-> It creates a package.json file for your project

-> Install dependencies in package.json file using : sudo npm i <dependencies> --save

##Adding Firebase to your Project :

-> Install Firebase tools using : sudo npm install -g firebase-tools

-> Then , first login to your firebase account using : firebase login 

-> It will redirect to you a Firebase CLI page , where you have to login using your firebase account

-> You can check the logged in account using firebase login in your console

-> Similary , you can log out using : firebase logout

-> Now, Initialize Firebase in your project : firebase init

->It asks you some information , which is given below :

=== Firebase CLI features  (Choose Database , Functions and Hosting here)
 ◯ Database: Deploy Firebase Realtime Database Rules
 ◯ Firestore: Deploy rules and create indexes for Firestore
 ◯ Functions: Configure and deploy Cloud Functions
 ◯ Hosting: Configure and deploy Firebase Hosting sites
 ◯ Storage: Deploy Cloud Storage security rules

=== Project Setup : You can use a existing project in your firebase account or you can create a new one here

=== Database Setup :  Use database.rules.json file

=== Functions Setup : 
	-Choose JavaScript
	-Install dependencies using y (when It asks)
	-Choose public directory : (.)

-> After finishing the initialization , it will create some files in your project (firebase.json , database.rules.json, functions etc.)

-> Now change the rules in database.rules.json : read and write => true

-> Check firebase.json (public should be .) 

-> Here , we have successfully completed our set up for firebase

##Using Firebase commands :

-> After writing your codes and files , you have to deploy it to firebase using : firebase deploy (It takes some time)

-> It will also give you a hosting url

-> If you only want to deploy functions or hosting, you can use : firebase deploy --only(functions/hosting)

-> To Run it on your localhost, you can also use : firebase serve

##For Notifications :

-> We are generating tokens for every subscription of user and storing them into firebase real time database

-> Whenever we want to send the notification , we access the firebase tokens and send the notifications to all those users

-> You can refer to :
	-index.html (for subscription page)
	-main.js (for generating and storing the tokens)
	-index.js (for sending the notifications)

##Other important keyterms , you may need to know about :

-> While Initializing the app , You have to require some modules (eg. firebase-functions and firebase-admin)

-> So, Give correct path of these packages

-> server key : (Go to firebase account->Settings->project settings->Cloud messaging)

-> sender_id  : (Go to firebase account->Settings->project settings->Cloud messaging)

-> Private Key : (Go to firebase account->Settings->Service accounts)

-> databse url : (Go to Database)

-> hosting url : (Go to Hosting, It also shows about recent deployments)

-> Logs : (Go to Functions->Log)




