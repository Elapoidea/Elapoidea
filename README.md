```rust
fn pascal(rows: usize) -> Vec<Vec<usize>> { 
    (0..rows).map(|r| {
        (1..=rows-r).map(|n| {
            (n..=n+r-1).product::<usize>() / (1..=r).product::<usize>()
        }).collect()}).collect()}
```
