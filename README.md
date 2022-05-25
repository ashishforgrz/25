# 25/05/2022

Callback - 
function passed as an argument to another function

function which is to be executed after another function has finished execution.

Types of callbacks - 

Synchronous callbacks -
executed during the execution of the higher-order function that uses the callback
synchronous callbacks are blocking   :   the higher-order function doesn't complete its execution until the callback is done executing
eg: 

function greeting(name) {

  alert('Hello ' + name);
  
}

function processUserInput(callback) {

  var name = prompt('Please enter your name.');
  
  callback(name);
  
}

processUserInput(greeting);


Asynchronous callbacks -
executed after the execution of the higher-order function
asynchronous callbacks are non blocking  :  the higher-order function completes its execution without waiting for the callback
eg:

function printString(){

   console.log("Tom"); 
   
   setTimeout(function()  { 
   
   console.log("Jacob"); }, 300); 
   
  console.log("Mark")
  
}

printString();

The main difference between synchronous and asynchronous callbacks is that synchronous callbacks are executed immediately, whereas the execution of asynchronous callbacks is deferred to a later point in time.


Promise - 
Promise object represents the eventual completion or failure of an asynchronous operation and its resulting value
eg:

const demoPromise= function() {
  myFirstPromise
  .then((successMsg) => {
      console.log("Success:" + successMsg);
  })
  .catch((errorMsg) => { 
      console.log("Error:" + errorMsg);
  })
}
demoPromise();

we use then() for resolve and catch() for reject any promise



Async and Await -
async makes a function return a Promise
await makes a function wait for a Promise

an async function without an await expression will run synchronously
