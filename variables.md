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

