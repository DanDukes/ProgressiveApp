# Progressive Budget Tracker
[Deployed Link](https://dandukes-budget.herokuapp.com/)

[Github Repo](https://github.com/DanDukes/ProgressiveApp/)

## Author

Dan "Dukes" DeGeare

dan@degeare.com

[LinkedIn](https://www.linkedin.com/in/danieldegeare/)

[GitConnected](https://gitconnected.com/dandukes)

![landing](https://raw.githubusercontent.com/DanDukes/ProgressiveApp/master/public/images/main.png)

 ![Adding exercise](https://raw.githubusercontent.com/DanDukes/ProgressiveApp/master/public/images/demo.gif)


## Purpose
A Progressive Budget tracker powered by Node, Express, Mongo, and IndexedDB

## Functionality
The Budget App works my simply adding an amout and then either clicking add for a deposit or subtract for a withdrawl.  The total recalculates with each update and the chart redraws itself to keep a view of the running talley.  While online, the numbers are simply stored in a MongoDb database, which is interacted with via a RESTful API created with Mongoose and Express Router.

The App maintains is funtanality and synchonicity with the database when offline due to a combination of a registered Service Worker, ann a custom database javascript file loaded on the client side to keep track of transactions that cannot make it to Mongo in the local IndexedDB.  It will then sync the IndexedDB data with MongoDb in a bulk update as coon as connectivity is restored.

 ## Running locally

 1. Install any dependencies: ```npm install```;
 2. Start a local instance of MongoDb ```mongod``` /
 4. Run: ```npm start```;
 5. The default  port is *3000*, so to access you must go to **http://localhost:3000**

## Technologies
  * HTML, CSS, JavaScript, Bpptstrap 4, Node, Mongoose, Express(Router), IndexedDB
  
## Known Bugs/ Other Features
  * Still need additional validation on user input, the app currently does the bare minimum.
  
