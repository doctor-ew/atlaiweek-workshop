---
layout: default
---

# What the harness is made of

<div class="text-sm text-gray-400 mt-1">Three layers. Each one does a different job.</div>

<div class="grid grid-cols-3 gap-5 mt-6 text-sm">

<div class="rounded p-4 bg-purple-900/30 border border-purple-700/60 space-y-2">
<div class="text-purple-300 font-semibold font-mono text-base">CLAUDE.md</div>
<div class="text-purple-200 text-xs uppercase tracking-wider">The Contract</div>
<div class="text-gray-300 text-xs mt-2">Tells Claude what role it's playing, what pipeline it's running, and what constraints apply. Checked on every session start. The org-level one applies to every engineer automatically.</div>
<div class="mt-3 font-mono text-gray-500 text-xs">~/.claude/CLAUDE.md</div>
</div>

<div class="rounded p-4 bg-green-900/30 border border-green-700/60 space-y-2">
<div class="text-green-300 font-semibold font-mono text-base">workflows/cxeng/</div>
<div class="text-green-200 text-xs uppercase tracking-wider">The Stage Scripts</div>
<div class="text-gray-300 text-xs mt-2">One markdown file per stage. Each file is a precise checklist: what to read, what to produce, what artifact to write, what gate to call before moving on. Claude follows the file — not its own judgment.</div>
<div class="mt-3 font-mono text-gray-500 text-xs">01-init · 02-spec · 03-adversarial · 04-implement · 05-cxreview · 06-preflight</div>
</div>

<div class="rounded p-4 bg-amber-900/30 border border-amber-700/60 space-y-2">
<div class="text-amber-300 font-semibold font-mono text-base">settings.json hooks</div>
<div class="text-amber-200 text-xs uppercase tracking-wider">The Enforcement Layer</div>
<div class="text-gray-300 text-xs mt-2">Shell scripts that intercept Claude's tool calls at the OS level. Claude cannot write a file, call a tool, or move to the next stage without clearing the hook. This is not "please follow the process." It is enforced.</div>
<div class="mt-3 font-mono text-gray-500 text-xs">PreToolUse · PostToolUse</div>
</div>

</div>

<div class="mt-6 rounded p-3 bg-slate-800/60 border border-slate-600 text-xs text-center text-gray-300">
CLAUDE.md defines what to do. Workflows define how to do each step. Hooks make sure it actually happens.
</div>
