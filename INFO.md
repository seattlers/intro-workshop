# Workshop Info

Hi all!

We'd like to share some more details and setup tips for tomorrow's workshop.

## Goals

1. Help newcomers get up to speed with Rust.

2. Offer a project foundation that can be repurposed or taken in many different directions.

3. Learn "how to fish"/how to continue learning more on your own!

## Workshop Format

Working solo or in a pair/small group, you will build up a small Rust application. A series of prompts (with lots of hints and links) will guide you into iterating over the initial implementation. We will provide the prompts at the workshop. Note: you will need to bring a laptop!

We assume you have some prior general programming experience in at least one language, though it needn't be a compiled language. We do not assume ANY prior experience with Rust.

## Key Items

1. Attendees can work solo or in groups.

2. Work will be at each person/group's own pace.

3. Prompts will be approachable to folks with NO Rust experience.

## How to prepare

You will need a laptop.

We strongly encourage you to set up your Rust programming environment prior to coming to the event, to ensure you can just focus on the fun stuff while you're there.

Your environment is good to go if you can run something like the following:

(Mac/Linux example)
```
$ rustc --version
rustc 1.26.2 (594fb253c 2018-06-01)

$ cargo new workshop
     Created binary (application) `workshop` project

$ cd workshop/

$ cargo run
   Compiling workshop v0.1.0 (file:///home/joe/src/workshop)
    Finished dev [unoptimized + debuginfo] target(s) in 0.79s
     Running `target/debug/workshop`

Hello, world!
```

For help on this, see the Rust Book: https://doc.rust-lang.org/book/second-edition/ch01-03-hello-cargo.html

Make sure your laptop has the following installed:

1. Stable Rust

The recommended way to do this is via first installing the Rust toolchain manager, Rustup, but there are other options. As long as you have rustc (the compiler) and Cargo (the build/package manager), you will be ready for the workshop.

Rustup and other installation methods: https://www.rust-lang.org/en-US/other-installers.html

2. Programming text editor

You can use whatever you like: we won't need any fancy IDE features. If you're not sure what to use, we've found that many people seem to do fine with VS Code, which is cross-platform (Windows, Mac, and Linux).

VS Code: https://code.visualstudio.com/

That's it!

## Code of Conduct

The Seattle Rust Meetup follows the Rust Code of Conduct! Please check it out if you haven't already: https://www.rust-lang.org/en-US/conduct.html
