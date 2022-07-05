# Updates

---

UPDATE 25 June 2022:  
While learning the *Rust programming language* I discovered an interesting thing somewhat related to this...

*Rust* has 3 kinds of loops: `loop`, `while` and `for`. The `loop` variant can be *named* or labeled to easily refer to it when using nested loops.

The interesting part is HOW these loops are named in Rust. The name of the loop starts with a single quote i.e. our apostrophe!

Here's an example of using 2 nested loops in Rust:

```rust
fn main() {
    let mut count = 0;
    'counting_up: loop {
        println!("count = {}", count);
        let mut remaining = 10;

        loop {
            println!("remaining = {}", remaining);
            if remaining == 9 {
                break;
            }
            if count == 2 {
                break 'counting_up;
            }
            remaining -= 1;
        }

        count += 1;
    }
    println!("End count = {}", count);
}
```

Notice that `'counting_up` thingy. That's the label of the outer loop. That label is used the inner loop to break out of the loop.

But the cool thing is that the super-smart people developing the Rust programming language also came up with the same idea: Prepending a name with a single quotation mark symbol — our apostrophe — as an easy and terse way to denote something special. Yay! 

---
