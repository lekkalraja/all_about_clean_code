# all_about_clean_code

### What is Clean code ?
  * It's not about whether code works or not.
  * A Vast majority of time is spent `reading and understanding` code.
* `Clean Code`
    * Should be readable and meaningful
    * Should reduce cognitive load
    * Should be concise and "to the point"
    * Should avoid unintuitive names, complex nesting and big code blocks
    * Should follow common best practices and patterns
    * Should be fun to write and to maintain
### Key Pain Points
  * Names : `Variables, Functions & Classes`
  * Structure & Comments : `Code Formatting , Good & Bad Comments`
  * Functions : `Length & Parameters`
  * Conditional & Error Handling : `Deep Nesting, Missing Error Handling`
  * Classes & Data Structures : `Missing Distinction, Bloated Classes`
#### Solutions
  * Rules & Concepts
  * Patterns & Principles
  * Test-Driven Development

* Clean code `doesn't require Strong Typing`, 
  
  Types can help preventing errors and can improve readability 
  ```typescript
  function add(num1: number, num2: number) {
      return num1 + num2;
  }
  ```
  But code can also be 100% readable and meaningful without types
  ```python
  def add(num1, num2):
    return num1 + num2
  ```

## Embrace REFACTORING
  * Refactoring today is save time tomorrow
  * A codebase can only survive and stay maintainable if it's continuously improved and refactored
  * `Pro tip` : Whenever you add something new, try to improve existing code along the way


### Reference : https://github.com/academind/clean-code-course-code/tree/master