---
layout: default
---

# What actually goes wrong

<div class="grid grid-cols-2 gap-6 mt-6">

<div class="space-y-3">

<div class="rounded p-3 bg-red-950/50 border border-red-800/50 text-sm">
<div class="text-red-400 font-semibold mb-1">Hallucinated claims in the spec</div>
<div class="text-gray-300">AI references a method that doesn't exist. No one checks. Implementation fails at runtime.</div>
</div>

<div class="rounded p-3 bg-red-950/50 border border-red-800/50 text-sm">
<div class="text-red-400 font-semibold mb-1">Context compaction mid-ticket</div>
<div class="text-gray-300">Long session gets compressed. AI forgets the spec. Starts improvising against the original prompt.</div>
</div>

<div class="rounded p-3 bg-red-950/50 border border-red-800/50 text-sm">
<div class="text-red-400 font-semibold mb-1">Tests written after the code</div>
<div class="text-gray-300">Tests pass on day one because they were written to match the implementation, not the requirement.</div>
</div>

</div>

<div class="space-y-3">

<div class="rounded p-3 bg-red-950/50 border border-red-800/50 text-sm">
<div class="text-red-400 font-semibold mb-1">Review skipped or rushed</div>
<div class="text-gray-300">"AI already reviewed it." Drift between spec and code ships undetected.</div>
</div>

<div class="rounded p-3 bg-red-950/50 border border-red-800/50 text-sm">
<div class="text-red-400 font-semibold mb-1">No deployment record</div>
<div class="text-gray-300">Something breaks in staging. No one knows what changed or who approved it.</div>
</div>

<div class="rounded p-3 bg-green-950/50 border border-green-800/50 text-sm">
<div class="text-green-400 font-semibold mb-1">All of this is fixable</div>
<div class="text-gray-300">One pipeline. Every gate. Every time. No one has to remember the checklist.</div>
</div>

</div>

</div>
