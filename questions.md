
# Promise

## Promise Question 1
```js
// Promises in Javascript
// Ques 1- What's the output?
console.log("start");
const promise1 = new Promise((resolve, reject) => {
  console.log (1);
  resolve (2);
});
promise1.then((res) => {
  console.log (res);
});
console.log("end");
```


## Promise Question 2

```js
// Promises in Javascript
// Ques 2 - What's the output?
console.log("start");
const promise1 = new Promise((resolve, reject) => {
  console.log(1);
  resolve (2);
  console.log(3);
});
promise1.then((res) => {
  console.log(res);
});
console.log("end");
```

## Promise Question 3
```js
// Promises in Javascript
// Ques 3- What's the output?
console.log("start");

const fn = () =>
  new Promise ((resolve, reject) => {
    console.log (1);
    resolve("success");
  });

console.log("middle");

fn().then((res) => {
  console.log(res);
});

console.log("end");
```

## Promise Question 4
```js
// Promises Chaining Output
// Ques 4 - What's the output?

function job() {
  return new Promise(function (resolve, reject) {
    reject(); 
  });
}

let promise = job();

promise
.then(function () {
  console.log("Success 1");
})
.then(function () {
  console.log("Success 2");
})
.then(function () {
  console.log("Success 3");
})
.catch(function () {
  console.log("Error 1");
})
.then(function () {
  console.log("Success 4");
})
```

## Promise Question 5
```js
// Promises in Javascript
// Ques 5 - What's the output?
function job(state) {
  return new Promise (function (resolve, reject) {
    if (state) {
    resolve("success");
    } else {
    reject("error");
    }
  }); 
}

let promise = job(true);

promise
.then (function (data) {
  console.log(data);
  return job (false);
})
.catch(function (error) {
  console.log(error);
  return "Error caught";
})
.then(function (data) {
  console.log (data);
  return job(true);
})
.catch(function (error) {
  console.log(error);
});
```

## Promise Question 6
```js
// Promises in Javascript
// Ques 6 Promise Chaining
function job(state) {
  return new Promise (function (resolve, reject) {
    if (state) {
      resolve("success");
    } else {
      reject("error");
    }
  });
}

let promise = job(true);

promise
.then(function (data) {
  console.log (data);
  return job(true);
})
.then(function (data) {
  if (data !== "victory") {
  throw "Defeat";
  }
  return job(true);
})
.then(function (data) {
  console.log(data);
})
.catch(function (error) {
  console.log(error);
  return job(false);
})
.then(function (data) {
  console.log(data);
  return job(true);
})
.catch(function (error) {
  console.log(error);
  return "Error caught";
})
.then(function (data) {
  console.log(data);
  return new Error("test"); // Not Returning a promise
})
.then(function (data) {
  console.log("Success:", data.message);
})
.catch(function (data) {
  console.log("Error:", data.message);
});
```

## Promise Question 7
```js
// Ques 7- What's the output?

```

## Promise Question 8
```js
// Ques 8 - Rewrite this example code using `async/await`
// instead of `.then/catch`
function loadJson (url) {
  return fetch(url).then((response) => {
    if (response.status == 200) {
      return response.json();
    } else {
      throw new Error (response.status);
    }
  });
}

loadJson ("https://fakeurl.com/no-such-user.json").catch((err) =>
  console.log(err)
);

```

## Promise Question 9
```js
// Ques 9- Write a implementation

```