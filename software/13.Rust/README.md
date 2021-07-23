# Workshop 13 - Introduction to Rust

✔ The fundamentals of Rust.

✔ The standard Rust libraries.

✔ Data structures with Rust.

### Step 0 - SETUP

All the required information to install dependencies can be found in [SETUP.md](./SETUP.md).

> :bulb: We recommend you to follow the [Tour of Rust](https://tourofrust.com/index.html) for this workshop.

## Introduction to Rust

### Step 1 - Hello World! in Rust

> :exclamation: We strongly advise you to use the resources given for this exercise.

For the first exercise, we simply ask you to write `Hello world!` in your terminal when you run your program.

To do this, create a file `main.rs` in a folder called `src`.


> :bulb: Rust file has `rs` extension.

> :bulb: Now, that you have created a file `main.rs`, you can use other files. To use them in your `main.rs` you have to integrate the modulude with the keyword `mod` ([read more](https://stackoverflow.com/questions/26388861/how-to-include-a-module-from-another-file-from-the-same-project))

##### Resources

 - [Doc.Rust](https://doc.rust-lang.org/rust-by-example/hello.html)
 - [Build Commands](https://doc.rust-lang.org/cargo/commands/build-commands.html)

### Step 2 - Palindrome ?

> :exclamation: We strongly advise you to use the resources given for this exercise.

For the second exercise, you have to create a function that takes as parameter a string `word`.

Create a file `palindrome.rs` for this new function.

This function must return true if the word given in parameter is a palindrome and false in the opposite case.

##### Resources
 - [What is a palindrome ?](https://www.wikiwand.com/en/Palindrome)
 - [New function](https://doc.rust-lang.org/book/ch03-03-how-functions-work.html)
 - [The `bool` in Rust](https://doc.rust-lang.org/std/primitive.bool.html)

> :bulb: To easily test your functions during this workshop, we advise you to look at this tool. [`assert_eq`](https://doc.rust-lang.org/std/macro.assert_eq.html)

### Step 3 - Fibonacci sequence

> :exclamation: We strongly advise you to use the resources given for this exercise.

Create a file `fibonacci.rs` for this new function.

For the third exercise, create a function that takes one parameter:
- A number `max` with type `usize` that represent the number of element to compute.

You must now display the sequence of Fibbonaci from the number of starts to the maximum value.

Here is a small example of the beginning of the Fibonacci sequence :

```shell
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, ...
```

##### Resources
 - [Fibonacci number](https://www.wikiwand.com/en/Fibonacci_number)
 - [Match](https://doc.rust-lang.org/rust-by-example/flow_control/match.html)
 - [Vector](https://doc.rust-lang.org/std/vec/struct.Vec.html#indexing)

### Step 4 - Where is my vectors ?

In this exercise, you will transform vectors into a linked list.

To do this, you will create a file `to_list.rs`.

First, create a `linked_list` structure with the following attributes :
- `value: i32`
- `next` which has the structure type.

> :bulb: It's up to you to figure out how to initialize the structure to make a linked list.

In a second step, create a vector `vector` which will be transformed into a linked list.

As you will have understood, the objective of the exercise is to transform a vector into a linked list.

To do this, create a function `to_list` which takes `vector` as parameter and returns the list.

##### Resources
 - [List](https://rust-unofficial.github.io/too-many-lists/)
 - [Vector](https://doc.rust-lang.org/std/vec/struct.Vec.html#indexing)

### Step 5 - A simple and useful `Calculator` !

> :exclamation: We strongly advise you to use the resources given for this exercise.

Let's go further now!

The objective of this fifth exercise is to create a simplifying calculator.

Create a file `calculator.rs` for this new function.

To do this, you have to make a calculator that can do :
- `Addition`
- `Multiplication`
- `Division`
- `Subtraction`

between two values that must be retrieved one after the other from the user's input.

> :bulb: Pay attention to your error handling !

Display the result of the calculation in your terminal.

##### Resources
 - [Module std::io](https://doc.rust-lang.org/std/io/index.html)
 - [Examples io](https://doc.rust-lang.org/std/io/struct.Stdin.html#method.read_line)
 - [Option & unwrap](https://doc.rust-lang.org/rust-by-example/error/option_unwrap.html)
 - [Match](https://doc.rust-lang.org/rust-by-example/flow_control/match.html)

### Step 6 - Pig Latin

> :exclamation: We strongly advise you to use the resources given for this exercise.

The serious stuff begins!

This exercise is inspired by the `Pig Latin` concept, so feel free to look at the [original version](https://www.wikiwand.com/en/Pig_Latin) to help you.

Create a file `pig_latin.rs` for this new function.

Get a string as parameter, from this word you have to apply or not the following rules:

- If the word starts with a vowel, it doesn't matter. You just need to add a suffix `-hay` to your word.

- If the word starts with a consonant, you must take the first letter of the word and place it in the first position of the suffix.

> :bulb: To help you visualize the exercise, here are some examples :

```Rust
"PoC"        -->    "oC-Pay"
"Epitech"    -->    "Epitech-hay"
"Bumblebee"  -->    "umblebee-Bay"
"Although"   -->    "Although-hay"
```

> Well done! 🎉

Now that you can apply this to words, why not apply it to sentences?

As you can see, try to do the same thing, but for whole sentences.

To do this reuse the same function, but create a loop in your function.

> :bulb: Here are some examples too:

```Rust
"Live as if you were to die tomorrow. Learn as if you were to live forever."
-->
"ive-Lay as-hay if-hay you-hay ere-way o-tay ie-day omorrow-tay. earn-Lay as-hay if-hay you-hay ere-way o-tay ive-lay orever-fay."
```
```Rust
"A problem without a solution is a poorly stated problem"
-->
"A-hay roblem-pay ithout-way a-hay olution-say is-hay a-hay oorly-pay tated-say roblem-pay."
```

##### Resources
 - [Chars](https://doc.rust-lang.org/std/str/struct.Chars.html)
 - [Iterator](https://doc.rust-lang.org/std/iter/trait.Iterator.html)

## Bonus
Here are some bonus ideas if you want to venture further into the Rust adventure! 💪
 - Why not remake your Bistro-matic in Rust?

## Further reading
 - [The Rust website](https://www.rust-lang.org/fr)
 - [Tour of Rust](https://tourofrust.com/00_en.html)

## Authors
- [Yoel EDERY](https://www.linkedin.com/in/yoel-edery-957117210/)
- [Nicolas HEUDE](https://www.linkedin.com/in/nicolas-heude-525567197)

## Organization

- [📒 Linkedin](https://www.linkedin.com/company/pocinnovation/mycompany/)
- [📷 Instagram](https://www.instagram.com/pocinnovation/)
- [🖱️ Website](https://www.poc-innovation.fr/)
- [🌐 Discord](https://discord.gg/G4Aygn6p)

> :rocket: Don't hesitate to follow us on our different networks, and put a star 🌟 on `PoC's` repositories.
