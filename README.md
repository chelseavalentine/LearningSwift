# Syntax

### Super basic

```swift
print("Hello world!")
```

* `var` & `let`

  * with `let`, you can assign it only once

* you can use implicit typing, but explicit typing looks like:

  ```swift
  let explicitDouble: Double = 70 // 70.0
  ```

  * need to explicitly typecast

    ```swift
    let yo = "hey " + String(200)
    ```

* including variables values in strings

  ```swift
  let name = "Chelsea"
  let greeting = "Hi \(name)."
  ```

* arrays & dictionaries:

  ```swift
  // array
  var courses = ["Korean", "Algorithms", "CSO", "Transnational Asia"]
  courses[0] = "Intermediate Korean"

  // dictionaries
  // perfect example of what not to do, a dictionary is a set of key-value pairs where values are of the same type (I think?) it's not an object... (I think?)
  var person = [
    "name": "Chelsea",
    "age": 19,
    "wishes": [
    	"to sleep more",
      "to learn Swift"
    ],
  ]
  print(person["wishes"][0])
  ```

  * create empty arrays & dictionaries like so:

    ```swift
    // type will be inferred
    let emptyArray = []
    let emptyDictionary = [:]

    // explicit type declaring
    let emptyArray2 = [String]() // or whatever type you want
    let emptyDictionary2 = [String: Float]()
    ```



### Optionals… what?

* some variables can either be `nil` b/c its value is missing or have a value… they are called optionals

  ```swift
  var optionalString: String? = "The heck?"
  print(optionalString == nil)
  ```

* you can set a default value for when the optional is `nil`, by using `??`... do it like:

  ```swift
  let optionalName: String? = nil
  let defaultName: String = "John Smith"
  let greeting = "Is your name \(optionalName ?? defaultName)"
  ```



### Control flow

* `for-in` is like for each

  ```swift
  // with arrays
  for name in ["Chelsea", "Chelsea 2", "Chelsea 3"] {
    print(name)
  }

  // for dictionaries, which are iterated over in arbitrary order
  let stuff = [
    "favorite colors": ["Blue"],
    "favorite people": ["What?", "What??"],
    "uhhh...": ["what"],
  ]
  for (characteristics, values) in stuff {
    for characteristic in characteristics {
    	print("hehe")
    }
  }
  ```

* `if-else`

  ```swift
  if chelsea == "is cool" {
    points += 500
  } else {
    points = nil
  }
  ```

* optionals & control flows

  * you need to unwrapped optionals, and you can do so by using `let` and assigning the optional to your new variable like so:

    ``` swift
    var optionalName: String? = "Chelsea"
    var greeting = "Yo wut up?"
    if let name = optionalName { // if name isn't nil
      greeting = "Yo, wut up, \(name)?"
    }
    print(greeting)
    ```

    * the unwrapped variable `name` will have a scope of just the if statement (I think?)

* `switch` statements have implicit break statements

  ```swift
  let coolness = "So cool like wow"
  switch coolness {
  case "freaking lame":
    print("it looks like you are freaking lame")
  case "just okay", "alright, I guess...":
    print("it seems like you're alright")
  case let x where x.hasPrefix("so"):
    print("Congrats, you're as cool as Chelsea... \(x)")
  default:
    print("Why did I write this example")
  }
  ```

* `while`

  ```swift
  var n = 0
  while n < 2000 {
    print("chelsea is so cool")
    n++
  }
  ```

* `repeat-while` is the equivalent of do-while

  ```swift
  var m = 20
  repeat {
    print("chelsea is still so cool")
    m++
  } while m < 4000
  ```

* `for` loops

  ```swift
  for i in 0..<4 {
    print("well crap, im running out of creativity... \(i)")
  }

  // alternatively
  for var i = 0; i < 4; i++ {
    print("this feels more familiar")
  }
  ```

  * `..<` omits the upper value, `…` includes both values



### Functions & closures

* function `func`; `→ [return type]` cool.

  ```swift
  func greet(name: String, message: String) -> String {
    return "Hi \(name), a message was left for you:\n\(message)"
  }

  print(greet("Chelsea"), message: "Cool beans")
  ```

* tuples and functions, what? ok..

  ```swift
  p.12
  ```

  ​