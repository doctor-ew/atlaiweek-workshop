---
layout: default
---

# `/cxeng` flag reference

<div class="text-sm text-gray-400 mt-1">Every flag is a precision entry point. Default is the full pipeline.</div>

<div class="mt-5 grid grid-cols-2 gap-4 text-xs">

<div class="space-y-2">
<div class="text-gray-500 uppercase tracking-wider text-xs mb-3">Resume from a stage — run forward</div>

<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-gray-400 w-36 shrink-0">(no flags)</div>
  <div class="text-gray-300">Full pipeline — all 5 gates in sequence</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-amber-300 w-36 shrink-0">--from adversarial</div>
  <div class="text-gray-300">Skip spec production, start at adversarial</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-amber-300 w-36 shrink-0">--from implement</div>
  <div class="text-gray-300">Skip spec + adversarial, start at implementation</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-amber-300 w-36 shrink-0">--from cxreview</div>
  <div class="text-gray-300">Skip to drift + code quality review</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-amber-300 w-36 shrink-0">--from preflight</div>
  <div class="text-gray-300">Skip to preflight only</div>
</div>
</div>

<div class="space-y-2">
<div class="text-gray-500 uppercase tracking-wider text-xs mb-3">Run one gate only — stop after</div>

<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-green-400 w-36 shrink-0">--spec</div>
  <div class="text-gray-300">Spec stage only — stop after approval</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-green-400 w-36 shrink-0">--adversarial</div>
  <div class="text-gray-300">Adversarial verification only — stop after gate</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-green-400 w-36 shrink-0">--implement</div>
  <div class="text-gray-300">Implementation only — stop after tests pass</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-green-400 w-36 shrink-0">--review</div>
  <div class="text-gray-300">cxreview only — stop after APPROVE</div>
</div>
<div class="rounded p-3 bg-blue-950/40 border border-blue-700/40 flex gap-3">
  <div class="font-mono text-blue-300 w-36 shrink-0">--review --code-only</div>
  <div class="text-gray-300">Code quality only — skips Phase A drift check. Use when no spec exists yet but code needs review.</div>
</div>
<div class="rounded p-3 bg-slate-800/60 border border-slate-600 flex gap-3">
  <div class="font-mono text-green-400 w-36 shrink-0">--preflight</div>
  <div class="text-gray-300">Preflight + PR only</div>
</div>
</div>

</div>
