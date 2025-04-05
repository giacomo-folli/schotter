# Rust and Nannou Exploration

This repository is a collection of small projects to learn the Rust programming language and the [nannou](https://nannou.cc/) creative coding framework.

## Basic Setup Instructions

1.  Install Rust: [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install)
2.  Install nannou: Add `nannou = "0.19"` to your `Cargo.toml` file under the `[dependencies]` section.

## Project Structure

- `schotter1`, `schotter2`, `schotter3`: Each directory contains a separate nannou project.
- `src/main.rs`: Contains the main source code for each project.
- `Cargo.toml`: Contains the project dependencies and metadata.

## Code Examples

```rust
use nannou::prelude::*;

fn main() {
    nannou::app(model).update(update).run();
}

fn model(app: &App) -> Model {
    app.new_window().size(512, 512).view(view).build().unwrap();
    Model {}
}

struct Model {}

fn update(_app: &App, _model: &mut Model, _update: Update) {}

fn view(_app: &App, _model: &Model, frame: Frame) {
    let draw = app.draw();
    draw.background().color(WHITE);
    draw.ellipse().color(STEELBLUE);
    draw.to_frame(app, &frame).unwrap();
}
```

## Future Implementations

- Explore different nannou examples and tutorials.
- Implement interactive elements (e.g., mouse input, keyboard input).
- Create more complex visual patterns and animations.
- Experiment with audio input and output.

## Contribution Guidelines

Contributions are welcome! Please submit a pull request with your changes.
