---
layout: post
title:  "Closures, Lifetimes, and Higher Ranked Types"
date: 2017-03-01
categories: Rust
---
So here is the thing. Can we write something like

```rust
use std::collections::HashMap;
let mut hashmap: HashMap<i32, i32> = HashMap::new();
let closure = |x| hashmap.entry(x).or_insert(x+1);
println!("{:?}", closure(2));
```

in Rust?

The answer is, unfortunately, no.
