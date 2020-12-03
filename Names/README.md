# Naming - Assigning Names to Variables, Functions, Classes, etc...

* Naming `Things` : Variables, Constants, Properties, Methods/Functions & Classes etc...
  * Names Should be `meaningful`


## Why Name Matters
  *   Well-Named `Things` allow readers to understand your code without going through it in detail
  
  * Bad Naming : To understand the below code need's to go through the full class or function definitions and all other code 
    ```typescript
    const us = new MainEntity(); // what is MainEntity and what us describes
    us.process(); // What process does, not sure

    if(login) {  // Not sure what login is may be const, boolean, function, or something else
        //....
    }
    ```

  * Good Naming : To Understand the code, we don't need to go through the full class or function definitions and all other code
    ```typescript
    const user = new User(); // Creating User object
    user.save(); // saving user

    if(isLoggedIn) { // isLoggedIn is boolean
        //
    }
    ```

  *   We will always not agree because there are lot of alternatives to name things

```typescript

const admin = new Admin(); // This is Readable

const admin = new AdminUser(); // And so is this

```

## How To Name Things Correctly

* Variables, Constants, Parameters : Data Containers -> `Use nouns or short phrases with adjectives`
* Functions, Methods : Commands or calculated values -> `Use Verbs or short phrases with adjectives`
* Classes : Use classes to create "things" -> `Use nouns or short phrases with nouns`

## Name Casing

* `snake_case` : Eg: is_valid, send_response (use for Variables, Functions, methods) ExLang : Python
* `camelCase`  : Eg: isValid, sendResponse (use for Variables, functions, methods) ExLang: Java, JS
* `PascalCase` : Eg: AdminRole, UserRepository (use for Classes/Interfaces) ExLang: Java, Python, JS
* `kebab-case` : Eg: <side-drawer> Exlang: HTML (Custom HTML Elements)

## Naming Variables, Constants & Properties

* If Value is Object -> Describe the value (eg: authenticatedUser, sqlDatabase)
* If Value is Number & String -> Describe the value (eg: firstName, age)
* If Value is Boolean -> Answer a true/false question (eg: isActiveUser/loggedIn)

## Naming Functions & Methods

* If Function performs an operation -> Describe the operation (eg: getUser(), response.send())
* If Function computes a Boolean -> Answer a true/false question (eg: isValid(), purchase.isPaid())

## Naming Classes

* Describe the Object -> Avoid redundant suffixes

###### Note: Always provide more details without introducing redundancy

* Names should avoid describing unnecessary or redundant details
* Avoid Slang, Unclear Abbreviations & Disinformation
* Choose Distinctive Names
* Be Consistent