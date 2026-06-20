Terminal window chrome (hero centerpiece of the website) — traffic-light dots, muted title, dark body with colored mono lines.

```jsx
<TerminalWindow title="operator@ubuntu: ~">
  <div><span className="prompt">$</span> sudo ./armactl</div>
  <div className="output">[+] Detecting existing installation...</div>
  <div><span className="ok">[+] Service: active (running)</span></div>
  <div><span className="prompt">$</span> <TerminalCursor /></div>
</TerminalWindow>
```

- Line classes: `prompt` (green $), `output` (muted), `ok` (green), `warn` (orange), `info` (blue).
