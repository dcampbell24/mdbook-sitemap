# mdbook-sitemap

[![Crates.io](https://img.shields.io/crates/v/mdbook-sitemap.svg)](https://crates.io/crates/mdbook-sitemap)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Tool to generate a sitemap.xml file for an mdbook project

This tool is an mdBook backend that automatically generates a sitemap.xml

file when `mdbook build` is run. It reads the book structure from stdin
(as JSON provided by mdbook) and writes sitemap.xml to the output directory.

# Usage

1. Install `mdbook-sitemap`

```bash
cargo install mdbook-sitemap
```

OR

```bash
cargo binstall mdbook-sitemap
```

2. Add config to your `Book.toml`

```toml
[output.html]

[output.sitemap]
base-url = "https://example.com/docs/"
# Optional settings:
# change-freq = "weekly"          # always|hourly|daily|weekly|monthly|yearly|never
# priority = 0.7                  # 0.0 - 1.0
# output-filename = "sitemap.xml" # output filename
# include-draft = false           # whether to include draft chapters
```

# Install in Github Actions

```
- name: Install mdbook plugin
  run: curl --proto '=https' --tlsv1.2 -LsSf https://github.com/sonneko/mdbook-sitemap/releases/latest/download/mdbook-sitemap-installer.sh | sh
```

# Licence

MIT license
