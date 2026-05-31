---
layout: two-cols
---

# We observe everything

<div class="text-sm text-gray-400 mt-1">Every stage transition emits a structured event. Pipeline health is a Datadog query away.</div>

<div class="mt-5 space-y-2 text-xs">

<div class="rounded p-3 bg-slate-800/60 border border-slate-600">
<div class="text-green-300 font-mono mb-1">cxeng.stage spec start</div>
<div class="font-mono text-gray-500 text-xs">stage: spec · transition: start · ticket: IP-48</div>
<div class="font-mono text-gray-500 text-xs">engineer: drew@doctorew.com · version: 1.0.0.20260528-2310</div>
</div>

<div class="rounded p-3 bg-slate-800/60 border border-slate-600">
<div class="font-mono text-amber-300 mb-1">cxeng.stage spec complete</div>
<div class="font-mono text-gray-500 text-xs">duration_seconds: 6780 · bypass_flag: null</div>
</div>

<div class="rounded p-3 bg-slate-800/60 border border-slate-600">
<div class="font-mono text-amber-300 mb-1">cxeng.stage preflight complete</div>
<div class="font-mono text-gray-500 text-xs">bypass_flag: IP-42 · pr_url: azure-devops/...</div>
</div>

</div>

<div class="mt-5 grid grid-cols-2 gap-3 text-xs text-center">
<div class="highlight-box">
<div class="text-2xl font-bold text-green-400">5</div>
<div class="text-gray-400 mt-1">transitions per stage</div>
<div class="text-gray-500 text-xs">start · complete · error · skip · abandon</div>
</div>
<div class="highlight-box">
<div class="text-2xl font-bold text-amber-400">0</div>
<div class="text-gray-400 mt-1">engineer setup steps</div>
<div class="text-gray-500 text-xs">credentials via org-managed settings</div>
</div>
</div>

<div class="mt-4 text-gray-500 text-xs italic text-center">
Fire-and-forget. 3s timeout. Pipeline never blocks on telemetry.
</div>

::right::

<div class="pl-4 h-full flex flex-col justify-center">
<img :src="'/datadog-cxeng.png'" class="rounded-xl border border-slate-600 shadow-2xl w-full" />
<div class="mt-3 text-center text-gray-500 text-xs">
Real event from IP-48 · May 28, 2026<br>
<span class="text-amber-400">This pipeline built its own telemetry. Then we watched it ship.</span>
</div>
</div>
