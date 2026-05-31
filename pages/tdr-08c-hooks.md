---
layout: default
---

# The hooks are what make it un-skippable

<div class="text-sm text-gray-400 mt-1">CLAUDE.md is instructions. Hooks are enforcement. The difference matters.</div>

<div class="grid grid-cols-2 gap-5 mt-5 text-xs">

<div class="space-y-3">
<div class="text-gray-400 text-xs uppercase tracking-wider mb-2">PreToolUse — blocks before the action</div>

<div class="rounded p-3 bg-slate-800/60 border border-amber-700/40">
<div class="font-mono text-amber-300 mb-1">briefing-gate.sh</div>
<div class="text-gray-300">Fires before <code>/cxeng</code> starts. Checks that an approved spec exists. No spec → no pipeline. Claude literally cannot proceed.</div>
</div>

<div class="rounded p-3 bg-slate-800/60 border border-red-700/40">
<div class="font-mono text-red-300 mb-1">scope-freeze.sh</div>
<div class="text-gray-300">Fires before every Edit or Write during implementation. Checks the declared scope file. Blocks edits outside the spec's "Files to Change" table. Claude cannot go off-script.</div>
</div>

</div>

<div class="space-y-3">
<div class="text-gray-400 text-xs uppercase tracking-wider mb-2">PostToolUse — validates after the action</div>

<div class="rounded p-3 bg-slate-800/60 border border-green-700/40">
<div class="font-mono text-green-300 mb-1">quality-gate.sh</div>
<div class="text-gray-300">Fires after each stage completes. Verifies the required artifact exists and passes a structural check. Missing or malformed → stage marked blocked, pipeline stops.</div>
</div>

<div class="rounded p-3 bg-slate-800/60 border border-blue-700/40">
<div class="font-mono text-blue-300 mb-1">cxeng-pr-gate.sh</div>
<div class="text-gray-300">Fires before <code>az repos pr create</code>. Checks that a signed preflight manifest exists. No manifest → PR creation is denied at the tool level.</div>
</div>

</div>

</div>

<div class="mt-5 grid grid-cols-2 gap-5 text-xs">

<div class="rounded p-3 bg-red-950/40 border border-red-800/40 text-center">
<div class="text-red-400 font-semibold mb-1">Without hooks</div>
<div class="text-gray-400">"Claude, please follow this process."<br>Depends on prompt fidelity and context window. Degrades silently.</div>
</div>

<div class="rounded p-3 bg-green-950/40 border border-green-800/40 text-center">
<div class="text-green-400 font-semibold mb-1">With hooks</div>
<div class="text-gray-400">"Claude cannot skip this step."<br>Enforced at the tool layer. Degrades loudly — you see the block, not the drift.</div>
</div>

</div>
