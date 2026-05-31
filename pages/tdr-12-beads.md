---
layout: default
---

# The local ledger: beads

<div class="text-sm text-gray-400 mt-1">Every pipeline run needs a ticket to anchor to. Beads is where that ticket lives — locally, versioned, readable by agents and humans.</div>

<div class="grid grid-cols-2 gap-6 mt-6">

<div class="space-y-3">

<div class="rounded p-4 bg-slate-800/60 border border-slate-600 text-sm">
<div class="text-amber-400 font-semibold mb-2">What it is</div>
<div class="text-gray-300">A local issue tracker built on <span class="text-white font-mono">Dolt</span> — a version-controlled SQL database. Issues are hash-addressed, dependency-aware, and fully auditable. Agents can read and write it natively.</div>
</div>

<div class="rounded p-4 bg-slate-800/60 border border-slate-600 text-sm">
<div class="text-amber-400 font-semibold mb-2">What it's not</div>
<div class="text-gray-300">Not a replacement for Jira, GitHub Issues, or Linear. It's the <span class="text-white font-semibold">local engineering ledger</span> — the agent's copy of "what am I working on right now."</div>
</div>

</div>

<div class="space-y-3">

<div class="rounded p-4 bg-slate-800/60 border border-slate-600 text-sm">
<div class="text-green-400 font-mono mb-2">bd show TDR-by0</div>
<div class="font-mono text-xs text-gray-400 space-y-1">
<div><span class="text-gray-500">title:</span> Leave By badge on ZonePicker</div>
<div><span class="text-gray-500">status:</span> open</div>
<div><span class="text-gray-500">external_ref:</span> TDR-1</div>
<div><span class="text-gray-500">acceptance:</span> 7 criteria</div>
<div><span class="text-gray-500">labels:</span> demo, live-build</div>
</div>
</div>

<div class="rounded p-4 bg-slate-800/60 border border-slate-600 text-sm">
<div class="text-amber-400 font-semibold mb-2">Why it matters here</div>
<div class="text-gray-300">The pipeline runs against a ticket ID. Beads is where we pre-staged the PRD we wrote this morning. <span class="font-mono text-green-400">/cxeng TDR-by0</span> knows exactly what to build — and when it's done, the ticket closes with a full artifact trail.</div>
</div>

</div>

</div>

<div class="mt-5 text-center text-gray-500 text-xs italic">
github.com/gastownhall/beads — local-first, agent-native, Dolt-powered
</div>
