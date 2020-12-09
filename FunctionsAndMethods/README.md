# Funcitons
* Be Concise - In Every Aspect

#### What Make's up a Function/Method ?

```python
def add(n1, n2):
    return n1 + n2
```
* Working with the function should be easy & Readable
* The length of the funciton body matters

```python
add(5, 7)
```
* Calling the function should be readable
* The number and order of arguments matter

### The Number of Function/Method Parameters
* Minimize the number of parameters
  * None : Easy to Understnad & Call. Best Possible Option
  * 1    : Easy to understand and call. Very good possible option
  * 2    : Decent to understand & Acceptable to call. Use with Caution
  * 3    : Challenging to understand & call. Avoid if possible
  * > 3  : Difficult to read, understand & call. Alwasy avoid.

* Try to avoid output arguments - especially if they are unexpected
    * createId(user) -> Not great - user gets modified in an unexpected way
    * addId(user) -> Okay - user gets modified, but the function implies it
    * user.addId() -> Great - It's obvious, that the user will get modified

* Functions should be `small`
* Function should do exactly `One Thing`

##### One Thing
    * `Different Operations` : Eg : Validate + Save User Input => Operation 1 + Operation 2
    * `Different Levels of Abstraction` : 
          Eg: 
          ```js
          email.includes('@') => Low-Level API Operation on a string

          saveUser(email, password) => High-level, developer-defined function for saving a user
          
          ```
* Understanding `Levels of Abstraction`
    * High Level => isEmail(email) => We don't control how the email is validated - we just want it to be validated. This is easy to read - there is no room for interpretation
    * Low Level -> email.includes('@') => We control how the email is validated. This might be technically clear, but the interpretation must be added by the reader

* Functions should do work that's `one level of abstraction below their name`
  ```python
  def email_is_valid(email):
    return email.contains('@')

  * This function should return yes/no (true/false) based on the email validity
  ```
  ```python
  def save_user(email):
    if (email.contains('@')) :
      .....
    .....

  * This function should orchestrate all the steps that are required to save a user
  ```
###### Try Not To Mix Levels of Abstractions

* Keeping functions short - Rule of Thumb
  * Extract code that works on the same functionality
  * Extract code that requires more interpretation than the surrounding code

###### Stay DRY - Don't Repeat Yourself (DRY) (Reusability Matters sometimes)
* DRY = "Don't Repeate Yourself" == Don't write the same code more than once
* Signs of code which "is not DRY"
    * You find yourself copy & pasting code
    * You need to apply the same change to multiple paces in your codebase

##### Don't Overdo it - Avoid Useless Extraction
* Opinion : Split functions reasonably
* Being as granular as possible won't automatically improve readability => The opposite might be the case!
* Make Reasonable decisions and don't split if
      * you're just renaming the operation
      * finding the new function will take longer than reading the extracted code
      * can't produce a reasonable name for the extracted function
#### Try Keeping Functions Pure
* The same input always yields the same output
* No side effects

##### What's a Side Effect ?
* A  `side effect` is an operation which does not just act on function inputs and change the function output but which instead `changes the overall system/program state`
* Side effects are not automatically bad - we do need them in our programs. But `unexpected side effects should be avoided`.
* The name of a funciton should signal or imply that a side effect is likely to occur => Naming Matters!

###### Handling Side Effects
* Your functions should `not` have any unexpected side effects
* If you have/need a side effect
      * Choose a function name which implies it
      * Move the side effect into another function/place

## Unit Testing Helps!
* Can you easily test a function ?
  * Yes => Great
  * No => Consider splitting it