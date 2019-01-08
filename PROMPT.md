1. Write a command-line binary that reads numbers in from the command line (as
   arguments) and computes some stats (min, max, mean, sum, size).

See if you can ensure that the stats are computed _iteratively_, so you don't
ever need to hold the entire data set in memory.

For example, you could have a struct like:

```rust
struct Stats {
    max: f64,
    mean: f64,
    min: f64,
    size: u64,
    sum: f64,
}
```

...with a method `update(&mut self, val: f64)` that, given the the stats so far
(`self`) and the value of the next sample point (`val`) computes the summary
stats for the new data set which includes `val`.

2. Read numbers from a file and compute stats on the file's numbers. You can
   just `panic!` if the file contains invalid lines, or the filename is invalid.

- Tip: try using a `BufReader`
- Link to `BufReader` example and docs:
  https://doc.rust-lang.org/beta/std/io/struct.BufReader.html#examples

3. Use `serde` and `serde_derive` to output the stats as valid JSON.

4. Add a `from_iter` ctor for `Stats` that accepts an iterator of f64 values as
   its argument, and returns a new `Stats` struct.

- Docs for the `Iterator` trait:
  https://doc.rust-lang.org/std/iter/trait.Iterator.html
- The Rust Book (2nd ed) chapter on iterators:
  https://doc.rust-lang.org/1.30.0/book/second-edition/ch13-02-iterators.html

5. Add your own error type that implements `std::error::Error`, and replace the
   `unwrap()` and panics with use of `?` and `Result`.

- Docs for the `Error` type:
  https://doc.rust-lang.org/beta/std/error/trait.Error.html
- Try using the `?` operator:
  https://stackoverflow.com/questions/42917566/what-is-this-question-mark-operator-about

6. Use `clap` to add a nicer CLI interface and allow an option that ignores
   blank lines in the input file.

- Clap home page: https://clap.rs/
- Clap example: https://docs.rs/clap/2.31.2/clap/#quick-example

7. Add a `DataFileIterator` struct that impls `Iterator` with and
   `Iterator::Item = f64`, and use that to encapsulate file handling.

- Writing your own iterator:
  https://doc.rust-lang.org/book/second-edition/ch13-02-iterators.html#creating-our-own-iterators-with-the-iterator-trait

8. Add a command-line option to read sample points from `stdin`.

- `Stdin` docs: https://doc.rust-lang.org/std/io/struct.Stdin.html
- Example of using `io::stdin` to read from stdin:
  https://doc.rust-lang.org/std/io/fn.stdin.html

9. Add a command-line option to write all computed stats to a file as JSON.

- Docs with example: https://doc.rust-lang.org/std/fs/struct.File.html
