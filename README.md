# Minimal Typst CV Template

A semantic, ATS-optimized Curriculum Vitae template built with Typst. Designed to ensure correct text extraction by automated parsers while maintaining a clean, structured layout.

## Features

* **ATS Optimization**: Uses a linear table layout to force correct reading order (Left → Right, Top → Bottom) for parsers, unlike floating text boxes in standard LaTeX/Word templates.
* **Semantic Structure**: Implements real PDF headings and embeds metadata (Title, Author, Keywords) for correct indexing.
* **Modern Typography**: Uses standard sans-serif fonts (Arial, Helvetica, Liberation Sans) for maximum compatibility across systems.
* **Modular**: Logic is isolated in `template.typ`, keeping content separate in `main.typ`.

## Usage

### Prerequisites

Install the Typst CLI:

```bash
# macOS
brew install typst

# Windows
winget install typst

# Cargo
cargo install typst-cli

```

### Configuration

1. **Clone the repository.**
2. **Edit `main.typ**`: Update the `#cv()` function with your personal details.
* Ensure `keywords` are relevant to your target role.
* Place your profile image in the root directory and update the `profile-picture` path.


3. **Customize Layout**: Modify `template.typ` only if you need to alter the grid structure or styling logic.

### Build

Generate the PDF:

```bash
typst compile main.typ cv.pdf

```

Watch for changes during development:

```bash
typst watch main.typ cv.pdf

```

## License

MIT License.
