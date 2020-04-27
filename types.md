## Types

One of the main functionalities of the programming languages is manipulating data. Let's imagine two number like 3 and 8. We can have the summa, multiplication and other data manipulations on these number by using programming languages.

But first we have to define what type of data we want to represent, since the computer don't know about what is the number and what are the sentences.

There are three major and basic category of data representation.

- Numerical data
- Character based data, or character sequences
- Logical value like true/false

### Numberical data

```go
package main

import (
	"fmt"
	"reflect"
)

func main() {
	fmt.Println(reflect.TypeOf(12)) // case 1

	fmt.Println(reflect.TypeOf(44123123)) // case 2

	fmt.Println(reflect.TypeOf(int16(332))) // case 3

	fmt.Println(reflect.TypeOf(33.423)) // case 4
}
```

[Playground](https://play.golang.org/p/Ez9l1RhWyG0)

Firstly talk about the imported new functionality. The `reflect` consist of a huge amount useful functionalities, but we should use the `reflect`'s `TypeOf` functionalities. This will show us what is the type of the data.

So if you run the code snippet above, the result will be types printed out on the console. So the most basic numerical type is the `integer`. It's called `int`, so in case of 1 and 2, we will see that the type of 12 and type of 44123123 will be `int` in both cases. Integer stores numbers from -2^63 to 2^63-1 range. So if we want to store 2^63 = 9,223,372,036,854,775,807 or bigger we can't because this is the upper limit of the integer data representation.

Most of the languages has different size of number data representation as you can see in case 3. This is not relevant in our case, so you can check it out on the other additional section. [Details of numerical data representation](additional-numberic.md)

In case 4 we see a new kind of numeric data representation. It's the floating-point number as `float64`. While the integer type stores integers the float-point number can store real numbers with float-point like 33.423. We can do the same manipulations on them, like summa, mutiplication, etc.

There is a strict restriction on data manipulation, they have to be the same type. So I can do summa on two integers, but I can't do on an integer with a float-pointer.

### Character based data, or character sequences

```go
package main

import (
	"fmt"
	"reflect"
)

func main() {
	fmt.Println("I'm a sentence.")
	fmt.Println(reflect.TypeOf("I'm a sentence."))
}
```

[Playground](https://play.golang.org/p/uZHTE1YqZBK)

As we used it in the previous section, everything between quotas are something called `string`. String can store a single character or a word over a whole sentence, sentences or you can store a content of a book in them.

So in the first place we print the "I'm a sentence." and then we get the type of it. It will print "string", so we proved that the type is `string`.

### Logical value like true/false

The most fundamental and useful datatype in programing is the logical decision type, the `bool`. It determine whether a phase/decision/etc. TRUE or FALSE. 
We will you is it in many places because decisions drive our code. As in the real life we make decisions in programming as well. 
We represent this two with `true` and `false` words, but not just these represent the actual values of the type. 
If I'm saying `10 == 10`, it will also represent a TRUE value.
If I'm saying `10 > 33`, it will also represent a FALSE value.
If I want to compare string types, like `"Programming is awesome" == "I'm awesome"` they aren't the same strings, so it will be also FALSE.

```go
package main

import (
	"fmt"
	"reflect"
)

func main() {
	fmt.Println(reflect.TypeOf(true))
	fmt.Println(reflect.TypeOf(false))
	
	fmt.Println(10 == 10)
	fmt.Println(10 > 33)
	fmt.Println("Programming is awesome" == "I'm awesome")
}
```
[Playground](https://play.golang.org/p/QUsTjbY6S0F)

So in the first two lines of the main functionality you can see that we ask the type of the `true` and `false`. It will be `bool` in both cases.
Then we test the examples and we can see that only the first compersion will be `true`. So we can see that all of the comparsions' result will be a `bool` type.

### Summary

In this section we have got a really basic understanding how the type systems works in programming languages. 
This is important, because in the further sections it's a must to know what type we want to use to represent certain data.
The first reason why I choose Go to write these, it's because the type system is so strict on purpose of easily understand types. 
Types are really important in programming, because it can give us safety on many other areas of programming.

Next section will have details on how we store these types in the memory.

[Variables >>](variables.md)
