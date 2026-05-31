---
layout: center
class: text-center
---

# Watch for the artifacts

<div class="text-gray-400 mt-2 text-base">The live build isn't about the feature. It's about what the harness creates.</div>

<div class="mt-8 grid grid-cols-2 gap-4 max-w-2xl mx-auto text-left text-sm">

<div class="rounded p-4 bg-purple-900/30 border border-purple-700/60">
<div class="font-mono text-purple-300 font-semibold mb-1">SPEC.md</div>
<div class="text-gray-400 text-xs">Written by /cxproduct. Defines what to build, acceptance criteria, and technical approach. This is the contract.</div>
</div>

<div class="rounded p-4 bg-blue-900/30 border border-blue-700/60">
<div class="font-mono text-blue-300 font-semibold mb-1">citations.jsonl</div>
<div class="text-gray-400 text-xs">Every function, field, and identifier in the spec — verified against the actual codebase. VERIFIED or NOT FOUND. No hallucinated claims make it through.</div>
</div>

<div class="rounded p-4 bg-green-900/30 border border-green-700/60">
<div class="font-mono text-green-300 font-semibold mb-1">REVIEW.md</div>
<div class="text-gray-400 text-xs">DRY · SOLID · ACID · CoC · BigO lenses. BLOCK / WARN / NOTE for each finding. Human signs off on findings before preflight.</div>
</div>

<div class="rounded p-4 bg-amber-900/30 border border-amber-700/60">
<div class="font-mono text-amber-300 font-semibold mb-1">PREFLIGHT.md</div>
<div class="text-gray-400 text-xs">Deployment manifest. Env vars, migrations, dependencies. Every checkbox confirmed — same interview, every ticket, every engineer.</div>
</div>

</div>

<div class="mt-8 text-gray-500 text-sm italic">
When something breaks six months from now — open the folder. Everything is there.
</div>
