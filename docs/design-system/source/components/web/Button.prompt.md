Outlined neon "ghost" CTA button from the armactl website — uppercase Roboto Mono, sharp corners, tint + glow on hover.

```jsx
<Button color="green" icon="fa-brands fa-github" href="https://github.com/dturovskiy/armactl/releases/latest">
  Download
</Button>
```

- `color`: `green` (primary), `blue` (secondary), `orange` (warning) — follow the accent role rules.
- `size="sm"` for compact contexts; `icon` takes a Font Awesome class.
- Never give it a border-radius or a filled background.
