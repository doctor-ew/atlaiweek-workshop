---
layout: default
---

# The "Works Cited" Pattern

<div class="text-sm text-gray-400 mt-1">Every stage produces a signed-off artifact. The next stage runs on that artifact — not on hope. When something breaks, you have a paper trail.</div>

<div class="grid grid-cols-7 gap-2 mt-6 text-center text-xs items-start">

<div class="rounded p-3 bg-purple-900/30 border border-purple-700/60">
<div class="text-purple-300 font-mono font-semibold mb-1">SPEC.md</div>
<div class="text-gray-400">What to build + AC</div>
</div>

<div class="flex items-center justify-center text-gray-500 text-lg pt-3">→</div>

<div class="rounded p-3 bg-blue-900/30 border border-blue-700/60">
<div class="text-blue-300 font-mono font-semibold mb-1">citations.jsonl</div>
<div class="text-gray-400">Every claim verified in code</div>
</div>

<div class="flex items-center justify-center text-gray-500 text-lg pt-3">→</div>

<div class="rounded p-3 bg-green-900/30 border border-green-700/60">
<div class="text-green-300 font-mono font-semibold mb-1">REVIEW.md</div>
<div class="text-gray-400">DRY · SOLID · ACID · CoC · BigO</div>
</div>

<div class="flex items-center justify-center text-gray-500 text-lg pt-3">→</div>

<div class="rounded p-3 bg-amber-900/30 border border-amber-700/60">
<div class="text-amber-300 font-mono font-semibold mb-1">DRIFT.md</div>
<div class="text-gray-400">Spec ↔ diff parity check</div>
</div>

</div>

<div class="mt-4 grid grid-cols-3 gap-4 text-xs text-left">

<div class="rounded p-3 bg-slate-800/60 border border-slate-600">
<div class="text-amber-400 font-semibold mb-1">Adversarial verify</div>
<div class="text-gray-400">Before a line of code is written, Claude searches the actual codebase for every function, field, and constant the spec mentions. Hallucinated identifiers surface as questions — not as bugs in production.</div>
</div>

<div class="rounded p-3 bg-slate-800/60 border border-slate-600">
<div class="text-amber-400 font-semibold mb-1">Drift check</div>
<div class="text-gray-400">After implementation, the spec's "Files to Change" table is crossed with the actual git diff. Anything in spec but missing from diff — or in diff but not in spec — is surfaced before preflight.</div>
</div>

<div class="rounded p-3 bg-slate-800/60 border border-slate-600">
<div class="text-amber-400 font-semibold mb-1">Preflight</div>
<div class="text-gray-400">Structured interview before merge. Every deployment variable, every dependency change, every migration is confirmed — same checklist, every time, no matter how tired you are.</div>
</div>

</div>

<div class="mt-5 text-center text-gray-400 text-xs italic">
Artifacts are what let a human review fast and trust what they're reading.
</div>
