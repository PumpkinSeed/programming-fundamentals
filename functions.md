## Functions

Previously we learn about how we store data in memory using variables and constant definition, but we didn't talk about what is the use of it.
So in first place we will describe where we can use these. 

Firstly I want to extend your knowledge about the `fmt`. As we talked about the `fmt` means format. So we can format our string by using the `fmt` functionalities.
Most of the languages has similar features like this, but this is currently a Go specific solution (or C-like solution). 

```go
package main

import (
	"fmt"
)

func main() {
	fmt.Printf("Hi, %s. You have %d new notification(s)\n", "Joe", 32)
}
```
[Playground](https://play.golang.org/p/iwt65ruRjNN)

This code will result the following string: `Hi, Joe. You have 32 new notification(s)`. If we change the printing functionality from `Println` to `Printf` we can have extra formatting toolset.
If you remember the `Println`, prints the string and ln (line new). The `Printf` functionality is similar, so print and format, but it doesn't have ln. 
So we manually add it: `\n`.

So we get this extra toolset, so if you place this formatting points in your string wou can use variables to fill these points. `%s` means you should fill this gap with a string.
`%d` means you should fill it with an integer. `"Hi, %s. You have %d new notification(s)\n"`, as you seen there is TWO formatting point, so you should add TWO extra parameter.
`"Joe"` is the first, will be placed on the formatting point of the `%s`, and `32` is the second will be placed on the formatting point `%d`.
You can use as many formatting points as you want, so another example can be:
 
`"Hi %s, the weather is %s. You have %d notifications. %s waiting for you at the %s"`
 
 If you add `"Joe"`, `"cloudy"`, `32`, `"Jane"` and `"Big Ben"`, you will get the following:
 
 `"Hi Joe, the weather is cloudy. You have 32 notifications. Jane waiting for you at the Big Ben"`
 
 ---
 
 Getting back to usage of variables.
 
 ```go
package main

import (
	"fmt"
)

func main() {
	var yourName string = "Joe"
	var weather string = "cloudy"
	var numOfNotifications int = 32
	var whoWaitingForYou string = "Jane"
	var where string = "Big Ben"
	
	fmt.Printf(
		"Hi %s, the weather is %s. You have %d notifications. %s waiting for you at the %s\n",
		yourName,
		weather,
		numOfNotifications,
		whoWaitingForYou,
		where,
	)
}
```
[Playground](https://play.golang.org/p/nn_3VGfO9kn)

We used the previous example with the difference that we store the parameters in variables. Since these variables doesn't change we could use constant definitions as well,
but I want to reuse this function later where these values will be change based on conditions (in the next section). This is one use-case among many others. 

---

We know how to use variables, so we can talk about functions. Function can be hard to understand, because it's abstract logic.
So we talked about extra functionalities, these function creates these extra functionalities, so we can call these functions from now. 
The theory behind the functions that they are waits some input, and based on this input they will return output for us. 
Let's imagine a cake. Cake has a size, it can be 20cm wide or 40cm wide. The size is the input here. The output will be how many slices do we have, 
but it's strongly depend on the size of the cake. So if we have a 20cm wide cake there will be 6 slices, if we have 40cm there will be 12 slices.
We will implement this function in the next section where we will talk about conditions. For now, we only talk about functions in details.

So functions can accept inputs, but it's not necessary. Functions can work without inputs as well. 
They can return outputs, but it's not necessary as well.

```go
package main

import (
	"fmt"
)

func main() {
	printHello()
	printMyName("Joe")
	fmt.Print(getNewLine())
}

func printHello() {
	fmt.Print("Hello ")
}

func printMyName(myName string) {
	fmt.Print(myName)
}

func getNewLine() string {
	return "\n"
}
```

