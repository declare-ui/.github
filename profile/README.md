<p align="left">
  <img width="1280" height="192" alt="DeclareUI" src="https://github.com/user-attachments/assets/d51c038f-7822-4ee4-beb8-f438894f7736#gh-light-mode-only" />
  <img width="1280" height="192" alt="DeclareUI" src="https://github.com/user-attachments/assets/44918531-3b1b-4ace-bca0-db0ea99f8bc8#gh-dark-mode-only" />
</p>

<h1 align="left">DeclareUI</h1>

<p align="left">
  <strong>Describe your UI. We'll build it.</strong>
</p>

<p align="left">
  Declare UI components in simple YAML and compile them to production-ready<br/>
  React, Vue, Angular, Svelte, or Web Components. One source, every framework.
</p>

<p align="left">
  <a href="https://declare-ui.github.io">Website</a> •
  <a href="https://github.com/declare-ui/core">Get Started</a> •
  <a href="https://github.com/declare-ui/docs">Docs</a> •
  <a href="https://github.com/declare-ui/mcp">AI / MCP</a>
</p>

---

### How it works

**1. Describe** — Write what you want in YAML. Props, layout, Tailwind styles. If you can describe it, you can build it.

```yaml
# button.ui.yaml — readable by anyone
component: Button
props:
  variant:
    type: enum
    values: [primary, secondary, ghost]
    default: primary
  label:
    type: string
    required: true
template:
  tag: button
  classes:
    base: "px-4 py-2 rounded-lg font-medium"
    variants:
      variant:
        primary: "bg-blue-600 text-white"
        secondary: "bg-gray-100 text-gray-900"
  children:
    - tag: span
      content: "$props.label"
```

**2. Preview** — See it live instantly. Tweak until it's right.

**3. Ship** — Export to any framework your team uses.

```bash
declareui build --targets react,vue,svelte,angular,wc
```

The output is native, idiomatic code — real React hooks, Vue Composition API, Svelte runes, Angular standalone components. Not wrappers. Full TypeScript types included.

---

### Ecosystem

| Repository | Description |
|:-----------|:------------|
| [`core`](https://github.com/declare-ui/core) | Parser, AST, validators & multi-target code generators |
| [`cli`](https://github.com/declare-ui/cli) | CLI tool — init, build, validate, test, preview |
| [`mcp`](https://github.com/declare-ui/mcp) | MCP Server — AI agents create components via natural language |
| [`components`](https://github.com/declare-ui/components) | Official library of 20+ production-ready UI components |
| [`tailwind-plugin`](https://github.com/declare-ui/tailwind-plugin) | Tailwind integration — build-time extraction, Shadow DOM, design tokens |
| [`vscode`](https://github.com/declare-ui/vscode) | VS Code extension — autocomplete, preview, AI-assisted editing |
| [`playground`](https://github.com/declare-ui/playground) | Interactive web playground |
| [`docs`](https://github.com/declare-ui/docs) | Documentation site |
| [`create-declareui`](https://github.com/declare-ui/create-declareui) | Project scaffolding — `npx create-declareui` |
| [`examples`](https://github.com/declare-ui/examples) | Example projects per framework |

---

### Who is DeclareUI for?

- **Backend devs** — "I'd rather describe than code the UI by hand"
- **Indie hackers** — "I want to prototype fast without framework lock-in"
- **Designers** — "I think in design. DeclareUI thinks in code."
- **PMs** — "I want to contribute real components, not just specs"
- **Frontend teams** — "One source, every framework"

---

### AI-native by design

DeclareUI ships with an **MCP Server** that lets AI agents like Claude, Cursor, and Windsurf create, modify, validate, and document components through conversation. You don't even need to write YAML — just describe what you want.

```json
{
  "mcpServers": {
    "declareui": {
      "command": "npx",
      "args": ["-y", "@declareui/mcp"]
    }
  }
}
```

> *"Create a DataTable component with sorting, pagination, and search filter."*
>
> → The agent generates valid `.ui.yaml`, validates the schema, and compiles to your target frameworks.

---

### Quick start

```bash
npm install -g @declareui/cli
declareui init my-design-system
cd my-design-system
declareui build --targets react,vue
```

---

<p align="center">
  <sub>Open source · MIT License · Built for every kind of builder.</sub>
</p>
