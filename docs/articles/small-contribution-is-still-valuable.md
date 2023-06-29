---
title: A small contribution is still valuable
published: true
published_at: 2023-06-29 11:30 +0000
---

Many people think that in order to contribute to an open source project one must be an expert and the contribution must be something big.

I just made a very small contribution that I think can illustrate well how one can contribute even small things and even without knowing the programming language.

I started to learn Rust maybe a week ago. It is not any easy language to learn and thus I hardly understand it. Its libraries are called "crates"
and I tried to use the [Handlebars](https://crates.io/crates/handlebars) crate which is the Rust implementation of the template system
that I think originated in [JavaScript Handlebars](https://handlebarsjs.com/)

## Trying the example in the documentation

The documentation showed this **Quick start**.

```rust
use handlebars::Handlebars;
use serde_json::json;

fn main() -> Result<(), Box<dyn Error>> {
    let mut reg = Handlebars::new();
    // render without register
    println!(
        "{}",
        reg.render_template("Hello {{name}}", &json!({"name": "foo"}))?
    );

    // register template using given name
    reg.register_template_string("tpl_1", "Good afternoon, {{name}}")?;
    println!("{}", reg.render("tpl_1", &json!({"name": "foo"}))?);

    Ok(())
}
```

I copied it into my editor, updated the `Cargo.toml` configuration file adding the dependencies and then ran the `cargo run` command as one needs to do.
I got the following error:

```
error[E0405]: cannot find trait `Error` in this scope
 --> src/main.rs:4:33
  |
4 | fn main() -> Result<(), Box<dyn Error>> {
  |                                 ^^^^^ not found in this scope
  |
help: consider importing one of these items
  |
1 + use core::error::Error;
  |
1 + use std::error::Error;
  |
```

This is really annoying when projects have non-working examples, but what can we do. Sometimes it a mistake. Sometimes
this happens as the code changes and the maintainers forget to update the documentation. Sometimes the authors think
that by showing only the important parts and assuming the user knows how to import modules is better than showing a longer,
but fully functioning example.

## Reporting the problem

In any case I decided to [report it](https://github.com/sunng87/handlebars-rust/issues/589).
This report is already valuable both to the author of the project and to anyone else who might encounter the same issue.

## Fixing the problem

I could have stopped here, and actually that was my intention, but then I realized that Rust was actually helpful here and
even told me that I am missing a **use**-statement.

I added the following line to the code and it started to work.

```rust
use std::error::Error;
```

That's it.

Again, I could have stopped here. After all **I** already had a solution and who cares about the rest of the world, right?


## Sending a pull-request

However, I know that these little issues can be really annoying and if I can make the experience of someone a bit smoother, that will increase the level of happiness in the world... well, in reality I just wanted to feel good that I contributed to project written in Rust. I just wanted to be able to brag about it.

So I sent [this pull-request](https://github.com/sunng87/handlebars-rust/pull/590).

It is a single line of change to the documentation. Look [here](https://github.com/sunng87/handlebars-rust/pull/590/files) to se the actual change I sent.

## The success

Within about 3 hours the author has accepted my pull-request.

This does not happen always. I think there were a number of factors that made this possible.

* The project is actively maintained.
* I demonstrated the problem in the [bug report](https://github.com/sunng87/handlebars-rust/issues/589).
* The fix was [very simple](https://github.com/sunng87/handlebars-rust/pull/590/files) and it was connected to the bug report.
* The author was awake when I made the changes or got up soon after.

## Background requirements

Of course in order to this I already had to know how to open an issue, how to fork and clone a project, how to send a pull-request
and probably some other things I don't remember now. However, these are all things that are generic to all the open source projects on GitHub and are almost the same on GitLab as well. So if you don't know these yet, your first contributions will take much longer even if they are small. With some practice you will get used to this and you will reap the value of this investment of time for a long time.

