---
layout: default
---

# Works everywhere you work

<div class="text-sm text-gray-400 mt-1">Same harness. Same gates. Same artifacts. Whichever interface the engineer prefers.</div>

<div class="grid grid-cols-3 gap-4 mt-6 text-sm">

<div class="rounded p-4 bg-blue-900/30 border border-blue-700/50">
<div class="text-blue-300 font-semibold mb-2">Claude Desktop</div>
<div class="text-gray-300 text-xs">Mac · Windows. Native app. Full MCP surface, file-system access via permissions.</div>
</div>

<div class="rounded p-4 bg-purple-900/30 border border-purple-700/50">
<div class="text-purple-300 font-semibold mb-2">VS Code Extension</div>
<div class="text-gray-300 text-xs">In-editor. Inherits the open workspace. Side-by-side with your code.</div>
</div>

<div class="rounded p-4 bg-green-900/30 border border-green-700/50">
<div class="text-green-300 font-semibold mb-2">Terminal (Claude Code)</div>
<div class="text-gray-300 text-xs">Mac · Linux · WSL · Windows PowerShell. CI/CD friendly. Headless-capable.</div>
</div>

</div>

<div class="mt-6 grid grid-cols-2 gap-5 text-sm">

<div class="rounded p-4 bg-slate-800/60 border border-slate-600">
<div class="text-slate-300 font-semibold mb-2">Mac · Linux · WSL — two lines</div>
<div class="font-mono text-xs text-green-400 space-y-1">
<div>git clone &lt;CX-Claude_plugin&gt; ~/.connexure/CX-Claude_plugin</div>
<div>bash ~/.connexure/CX-Claude_plugin/.cx/resolve-and-sync.sh</div>
</div>
</div>

<div class="rounded p-4 bg-slate-800/60 border border-slate-600">
<div class="text-slate-300 font-semibold mb-2">Windows PowerShell — two lines</div>
<div class="font-mono text-xs text-green-400 space-y-1">
<div>git clone &lt;CX-Claude_plugin&gt; $HOME\.connexure\CX-Claude_plugin</div>
<div>pwsh -File $HOME\.connexure\CX-Claude_plugin\.cx\resolve-and-sync.ps1</div>
</div>
</div>

</div>

<div class="mt-5 grid grid-cols-3 gap-3 text-xs text-center">

<div class="rounded p-3 bg-blue-950/40 border border-blue-700/40">
<div class="text-blue-300 font-semibold mb-1">Auto-updates</div>
<div class="text-gray-400">SessionStart hook syncs on every session. Nothing to remember.</div>
</div>

<div class="rounded p-3 bg-green-950/40 border border-green-700/40">
<div class="text-green-300 font-semibold mb-1">Self-healing</div>
<div class="text-gray-400">Forgot the two-liner? <code>/cxeng CR-XXX</code> bootstraps on first run.</div>
</div>

<div class="rounded p-3 bg-slate-800/50 border border-slate-600">
<div class="text-slate-300 font-semibold mb-1">One install, all projects</div>
<div class="text-gray-400">Installs to <code>~/.claude</code>. Works in every repo, no per-project setup.</div>
</div>

</div>
