---
layout: default
---

# One command per role. Airlocks between them.

<div class="text-sm text-gray-400 mt-1">Each role gets one entry point. The harness handles the rest.</div>

<div class="grid grid-cols-4 gap-4 mt-6 text-sm">

<div class="rounded p-4 bg-purple-900/30 border border-purple-700/60">
<div class="font-mono text-purple-300 text-base mb-2">/cxproduct</div>
<div class="text-purple-200 text-xs uppercase tracking-wider mb-2">Product</div>
<div class="text-gray-300 text-xs">Briefing gate · three grounding questions · adversarial source-of-truth check · spec draft</div>
<div class="mt-3 text-xs text-purple-300 font-semibold">→ Spec approved</div>
</div>

<div class="rounded p-4 bg-green-900/30 border border-green-700/60">
<div class="font-mono text-green-300 text-base mb-2">/cxeng</div>
<div class="text-green-200 text-xs uppercase tracking-wider mb-2">Engineering</div>
<div class="text-gray-300 text-xs">Spec · adversarial verify · implement with TDD · cxreview · preflight + manifest</div>
<div class="mt-3 text-xs text-green-300 font-semibold">→ PR + manifest filed</div>
</div>

<div class="rounded p-4 bg-orange-900/30 border border-orange-700/60">
<div class="font-mono text-orange-300 text-base mb-2">/cxqa</div>
<div class="text-orange-200 text-xs uppercase tracking-wider mb-2">QA</div>
<div class="text-gray-300 text-xs">Test plan from spec · SDET automation · go/no-go · publishes to Sources</div>
<div class="mt-3 text-xs text-orange-300 font-semibold">→ Go decision recorded</div>
</div>

<div class="rounded p-4 bg-gray-700/40 border border-gray-500/60">
<div class="font-mono text-gray-200 text-base mb-2">manifest</div>
<div class="text-gray-300 text-xs uppercase tracking-wider mb-2">DevOps</div>
<div class="text-gray-300 text-xs">DevOps consumes the deployment manifest produced by <code class="text-green-300">/cxeng</code> — no separate command, no re-derivation</div>
<div class="mt-3 text-xs text-gray-200 font-semibold">→ Production</div>
</div>

</div>

<div class="mt-6 text-center text-gray-300 text-sm">
<span class="text-amber-400 font-semibold">Each command produces a signed-off artifact.</span> The next stage can only run on a signed artifact.
</div>

<div class="mt-3 text-center text-gray-500 text-xs">
That's the airlock. The pressure equalizes — or you don't open the door.
</div>
