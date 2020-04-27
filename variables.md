## Variables

So we have a basic knowledge about what kind of data we can have in programming, but how we can store it?
The primary storage in that case is the computer's memory. So we write date into the memory and read data from the memory, but that's something what we will talk about later.

```go
package main

import (
	"fmt"
)

func main() {
	var myAge int
	myAge = 344

	fmt.Println(myAge)
}
```
[Playground](https://play.golang.org/p/FAoIsF4pmaw)

So what we see now? This is how we store data (in that case integer type data) in the memory. The new phrase comes in, "Variable declaration". 
Variable declaration means that we reserve a small place in the memory, that we will store some kind of data here. This is looks like `var myAge int`.
`var` means that it will be a variable, `myAge` is the name or identifier how we want to access to this piece of memory, and the last part determine the type, `int`.
So we have a memory slot, but what do we have written on this memory slot? Since we will write data in the next line to this slot we can assume, that it's empty.
That's not true. All the types have an initial value. Initial value means that if we don't give any value to it, it will have it by default. 
The `int` type default value is 0 (zero). So if we modify the code a bit, and tweak a `fmt.Println(myAge)` before the `myAge = 344`, we will see that it prints 0.

Let's move on and examine what the next line doing. `myAge = 344` write a certain value into the previously reserved memory slot. 
This means, when we want to use the `myAge` variable, we will have the 344 as it's value. So the next `fmt.Println` will write 344 to the consol.

```go
package main

import (
	"fmt"
)

func main() {
	var myAge int = 344

	fmt.Println(myAge)
}
```

New phrase coming in, "Variable initialization". So the following code will do the same as above with only one difference. We didn't do the initialization in two different lines.
Programming languages have a functionality where they can have a predefined initial value, or in other words we initialize the variable.
So we have `var` again, we define the name again `myAge`, we have a type again `int` and initialize the value with `= 344`.

---

We can store data in the memory, but what we can store in memory? The correct answer is, everything represented by the type system.
 
```go
package main

import (
	"fmt"
)

func main() {
	var str string = "I'm awesome"
	fmt.Println(str)
	
	var num int = 344
	fmt.Println(num)
	
	var weight float64 = 166.32
	fmt.Println(weight)
	
	var isCool bool = true
	fmt.Println(isCool)
}
```
[Playground](https://play.golang.org/p/0phRoBrh9eZ)

As we seen in this example we can use any type, the important thing is to follow the words in the order of declaration or initialization.
So like: `var NAME_OF_VARIABLE TYPE_OF_VARIABLE` in case of declaration and `var NAME_OF_VARIABLE TYPE_OF_VARIABLE = INIT_VALUE_OF_VARIABLE` in case of initialization.

---

We called it variable, because it's value can change anytime, so the value of it is variable.

```go
package main

import (
	"fmt"
)

func main() {
	var str string = "I'm awesome"
	fmt.Println(str)

	str = "I'm still awesome"
	fmt.Println(str)

	str = "Last modification"
	fmt.Println(str)
		
	str = "Okay, one more"
	fmt.Println(str)
}
```
[Playground](https://play.golang.org/p/p0jMngBN1UM)

What we can see here, the first line of main initialize the `str` variable, so we reserve a memory slot for `str` and then write data to that memory slot, then we print it.
At the next place we still have the `str` variable with reserved memory and we write something else on that memory address. After the print we can see that the "I'm awesome" is gone and replaced with "I'm still awesome".
We follow this pattern, and change these anytime when we want. So after we examine what happening, there is two part: `str` on the left-side, and the value on the right-side.
So on the right-side we say, write this data representation to the memory slot identified on the left-side. So write "Okay, one more", to the `str`.

---

We talked about the variables, where they value continuously changing over time. There is another data representation which can be initialized with a value, but it's not changeable.
So we introduce `const`, constant data representation.

```go
package main

import (
	"fmt"
)

func main() {
	const PI float64 = 3.14
	fmt.Println(PI)
}
```
[Playground](https://play.golang.org/p/qtEUx7vPn8Q)

In this case we have the same with only one difference. We are using `const` instead of `var`. This means we initialize the memory slot with a certain value, and never chamge.
What happens if we want to change it?

```go
package main

import (
	"fmt"
)

func main() {
	const PI float64 = 3.14
	fmt.Println(PI)
	PI = 3.15 // THIS IS NOT WORKING!
}
``` 

Go will throw an error to us, `cannot assign to PI`, which means we can't give a new value to this variable, because it's not a variable, it's constant data representation.

### Summary

So we learned about how we can store and retrieve data in the memory. Also a really basic but really important aspect of programming. 
In the next section we will talk about where we can use these variables, and introducing functions, where we can split our code to smaller reusable pieces.

[Functions >>](functions.md) 