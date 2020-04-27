## Hello world

```go
package main

func main() {
    println("Hello world")
}
```
[Playground](https://play.golang.org/p/aGyl0wLcnqG)

"Hello world" is the most basic code what we can have. Consist of 4 lines of code, where the online line what we should know about is the `println("Hello world")`.
If you run it in the playground, you will see the "Hello world" on the bottom of the webpage. So the "print" means print the words to the output. 
The "ln" means that it's automatically press an enter after the printed line. Let's proof it. If you update the playground with the following new lines, you will see the differences.

```go
package main

func main() {
    println("Hello world")
    print("it's in the new line, ")  // new code
    println("it's not")              // new code
}
```

Most of the programming languages are having the print functionality by default. So if you want to print anything on the consol, you only have to use the print functionalities.
This means that someone already implemented it for us. Most of these functinalities are part of the programming language, and most of them are not. 
The differences are that the first one can be used without importing them, nor like the other one.

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello world")
}
```
[Playground](https://play.golang.org/p/q141qv9pNtJ)

In this case we import and extra functionality. That's the `fmt` which is adding formatting functionalities. All of these extra functionalities consist of inner functionalities.
We can use them on the same way as we used the println previously. So we want to use the `fmt`'s `Println` functionality, which has the same functionality as the `println` has previously.
Look for another example. 

```go
package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Println(math.Pow(11,4))
}
```
[Playground](https://play.golang.org/p/iOzNMb2B-nh)

So we imported the `math` functionality. The `math` has a functionality to calculate a custom number on the nth power. In that example 11 on the 4th power which will be 14641.
So the result of math.Pow(11, 4) will be 14641, and because we used the `fmt`'s `Println` functinality, it will print the result out. 
The flow:
1. `math.Pow(11,4)` calculates the result.
2. The `Println` gets the 14641, to print it out.
3. `fmt.Println` prints the result to the consol.

## What happens behind the scenes

The program code what we are writing is a high level abstraction of the programming of the computer. There is a language called Assembly, which is the lowest level of the programming, but we don't want to leanr it... yet.
So the computer doesn't understand the code what we are writing by default. There is a translater or compiler which translates the code to something which is more understandable for the computer.
At the momment we are using a web based helper which doing it for us, just to test out the code. 
You can install this translater on your on computer as well. [Installation guides](install.md)

If you installed or you want to skip it for later, you can go with the next lesson.

### Summary 

In this section we learned the necessary tools to start learning programmings deeper and can visualize what we have done. These are the print functionalities. 
The next section will have basic details about types. 

[Types >>](types.md)