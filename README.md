# BAT Obfuscator v2

<img width="1079" height="1018" alt="1000084799" src="https://github.com/user-attachments/assets/64ce3708-5efd-4919-b05f-909eee87bccc" />


Pure Batch obfuscator with a terminal-inspired interface.

![Pure Batch](https://img.shields.io/badge/Pure-Batch-39ff14?style=flat-square)
![No PowerShell](https://img.shields.io/badge/No-PowerShell-blue?style=flat-square)
![Client-side](https://img.shields.io/badge/Runs-Client--side-orange?style=flat-square)

## Overview

BAT Obfuscator v2 is a browser-based tool that obfuscates Windows Batch (`.bat` / `.cmd`) scripts using only pure Batch-compatible techniques. It runs entirely in the browser — no server, no uploads, no PowerShell.

The tool combines stable techniques inspired by public projects such as Abobus and Somalifuscator, while deliberately avoiding methods that commonly break legitimate scripts.

## Features

<img width="1080" height="1051" alt="1000084802" src="https://github.com/user-attachments/assets/e300fee2-0987-451e-8621-90c9e64fc378" />


- **Substring reconstruction** (`%var:~n,1%`)
- **Environment-variable style alphabet**
- Safe random `@` and `;` prefixes
- Controlled case randomization
- Optional Anti-Echo checks
- Optional Anti-VM heuristics
- Dead code / opaque predicates
- Label & GOTO noise
- Three strength presets: Light / Medium / Heavy

## Presets

| Preset  | Description                                      |
|---------|--------------------------------------------------|
| Light   | Minimal changes, high readability                |
| Medium  | Balanced obfuscation (recommended default)       |
| Heavy   | Maximum stable obfuscation + optional protections|

## Usage

1. Open `index.html` in any modern browser
2. Paste your Batch code or upload a `.bat` / `.cmd` file
3. Choose a preset or enable individual options
4. Click **Obfuscate**
5. Download or copy the result

## Design Goals

- Pure Batch output only
- As aggressive as possible without breaking normal scripts
- Clean, readable terminal-style UI (vibrant green on dark)
- Fully client-side (privacy-friendly)

## Limitations

Batch is an interpreted language with significant constraints. This tool does **not** provide:

- Real encryption
- Strong anti-analysis
- Protection against determined reverse engineers

It significantly increases the effort required for casual inspection and automated simple analysis.

## File Structure

```
bat-obfuscator-v2/
├── index.html      # Single-file application (UI + engine)
└── README.md       # This file
```

## License

For educational and authorized use only.
