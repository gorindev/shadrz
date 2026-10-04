# ShadRz

A component distribution system, CLI, and customizable UI showcase for Blazor and .NET MAUI, built on top of **BaseRz** headless primitives.

Inspired by the philosophy of `shadcn/ui`, `ShadRz` is **not a traditional component library**. Instead of installing locked dependencies, you use the CLI to copy fully customizable Razor component source code directly into your repository.

---

## Features

- **You Own the Code:** Components are copied into your project so you can modify markup, styles, and behaviors freely.
- **CSS Framework Agnostic:** Supports multiple styling systems including **Tailwind CSS**, **Bootstrap**, and **StyleX / Scoped CSS**.
- **Powered by BaseRz:** Built-in accessibility, keyboard navigation, and headless state handling.
- **Cross-Platform Ready:** Sane defaults designed to run seamlessly in both browser and .NET MAUI Blazor Hybrid environments.
- **Interactive Playground:** Live documentation site allowing real-time theme swapping and code copying.

---

## CLI Quick Start

### 1. Install the CLI Tool

Install `ShadRz.CLI` globally via .NET tools:

```bash
dotnet tool install -g ShadRz.CLI
```

### 2. Initialize your Project

Run the initialization command in your Blazor or .NET MAUI root directory:

```bash
shadrz init
```

You will be prompted to choose your preferred styling adapter:

- Tailwind CSS
- Bootstrap
- StyleX / Scoped CSS

### 3. Add Components

Copy ready-to-use styled components into your project:

```bash
shadrz add dialog
shadrz add dropdown-menu
shadrz add button
```

---

## Usage Example

Once injected by the CLI, use components as local Razor source files:

```cshtml
<Dialog>
    <DialogTrigger class="btn btn-primary">
        Open Dialog
    </DialogTrigger>
    <DialogContent>
        <DialogTitle>Account Settings</DialogTitle>
        <DialogDescription>
            Update your profile preferences below.
        </DialogDescription>
        <DialogClose class="btn btn-secondary">Close</DialogClose>
    </DialogContent>
</Dialog>
```

---

## Repository Architecture

```plaintext
ShadRz/
├── src/
│   ├── ShadRz.CLI/           # CLI tool source code (.NET Global Tool)
│   │   ├── Commands/         # init, add, theme commands
│   │   └── Templates/        # Razor & CSS component code generators
│   ├── ShadRz.Components/    # Reference design system implementations
│   └── ShadRz.Docs.Web/      # Interactive Showcase & Live Playground app
└── tests/
    ├── ShadRz.CLI.Tests/     # Integration tests for code generation
    └── ShadRz.Components.Tests/ # Visual rendering & bUnit tests
```

---

## License

Distributed under the MIT License. See `LICENSE` for details.
