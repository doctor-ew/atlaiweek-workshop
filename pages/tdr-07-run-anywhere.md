---
layout: default
---

# Run from anywhere in the pipeline

<div class="text-sm text-gray-400 mt-1">Already reviewed? Just need the preflight? Skip ahead. Or stop early.</div>

<div class="grid grid-cols-2 gap-5 mt-6 text-sm">

<div class="rounded p-4 bg-slate-800/60 border border-slate-600">
<div class="text-slate-300 font-semibold text-xs uppercase tracking-wider mb-2">Resume from a stage — run forward</div>
<div class="font-mono text-green-400 text-sm space-y-1">
<div>/cxeng CR-295 <span class="text-amber-300">--from adversarial</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--from implement</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--from cxreview</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--from preflight</span></div>
</div>
</div>

<div class="rounded p-4 bg-slate-800/60 border border-slate-600">
<div class="text-slate-300 font-semibold text-xs uppercase tracking-wider mb-2">Run one gate only — stop after</div>
<div class="font-mono text-green-400 text-sm space-y-1">
<div>/cxeng CR-295 <span class="text-amber-300">--spec</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--adversarial</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--implement</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--review</span> <span class="text-gray-500 text-xs">[--code-only]</span></div>
<div>/cxeng CR-295 <span class="text-amber-300">--preflight</span></div>
</div>
</div>

</div>

<div class="mt-5 text-center text-gray-400 text-xs">
Default is the full pipeline. Flags exist for when you know exactly what you need.
</div>

<div class="mt-3 text-center text-gray-500 text-xs italic">
<code>--review --code-only</code> skips drift check — for tickets with no spec yet but code that needs review.
</div>
