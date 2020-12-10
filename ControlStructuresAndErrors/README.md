# Control Structures
* Code smart, Not Verbose

#### Keep Your Control Structures Clean
* Avoid Deep Nesting
    * Using Factory Functions & Polymorphism
    * Utilizing Errors
* Prefer Positive checks (if isEmpty over if isNotEmpty)

##### Use Guards & Fail Fast
```javascript
if (email.includes('@')) {
    // do stuff
}

Instead of Above approach Use Gurad & FailFast technique

// Guard
if (!email.includes('@')) {
    return ; // FailFast
}
// do stuff
```

```javascript
if(user.active) {
    if (user.hasPurchases()) {
        // do stuff
    }
}

Instead of Above

// Guard
if(!user.hasPurchases()) {
    return; // FailFast
}

if(user.active) {
    //do stuff
}
```

## Embrace Erros & Error Handling
* Throwing + Handling errors can replace if statements and lead to more focused functions
* simple rule : If something is an error => make it an error

```javascript

if(!isEmail) {
    return {code: 422, message : 'Invalid Input'}
}

if (!isEmail) {
    throw new Error("Invalid input")
}

```
###### Error Handling is `One Thing`!