# Concepts of Armstrong Numbers

## Example solution
```rust
pub fn is_armstrong_number(num: u32) -> bool {
    let digits = format!("{}", num);
    digits
        .chars()
        .map(|c| c.to_digit(10).unwrap().pow(digits.len() as u32))
        .sum::<u32>()
    == num
}
```

## General

- functions: integral to verifying solution, defining logic
- Test Suites: needed to verify solution
- `&str`: needed for counting the length of the number since Rust is strongly typed
- casting: required to apply arithmetic operations
- iterator features:
    - turbofish for brevity of function, single expression solution
    - `map` and `sum` for conviently reducing expression to what we need to assert
