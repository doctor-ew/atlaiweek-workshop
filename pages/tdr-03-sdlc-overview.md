---
layout: default
---

# The full SDLC — end to end
<div class="text-sm text-gray-400 mt-1">One command per role. Airlocks between them.</div>

<div class="grid grid-cols-6 gap-2 mt-4 text-xs">

<div class="rounded p-3 bg-purple-900/50 border border-purple-700/50">
<div class="text-purple-300 font-bold text-sm mb-2">Product Manager</div>
<div class="space-y-1 text-gray-200">
<div class="font-mono text-purple-300">/cxproduct</div>
<div class="text-gray-400">↓</div>
<div>Triage: valid?</div>
<div class="text-gray-400">↓</div>
<div>Draft / update PRD</div>
<div class="text-gray-400">↓</div>
<div>User discovery</div>
<div class="text-gray-400">↓</div>
<div class="text-purple-300 font-semibold">✓ PRD approved</div>
</div>
</div>

<div class="rounded p-3 bg-blue-900/50 border border-blue-700/50">
<div class="text-blue-300 font-bold text-sm mb-2">Engineering Lead</div>
<div class="space-y-1 text-gray-200">
<div>Draft TRD</div>
<div class="text-gray-400">↓</div>
<div>TRD approval</div>
<div class="text-gray-400">↓</div>
<div>Draft Spec</div>
<div class="text-gray-400">↓</div>
<div>Submit for review</div>
<div class="text-gray-400">↓</div>
<div class="text-blue-300 font-semibold">✓ Triad approved</div>
</div>
</div>

<div class="rounded p-3 bg-yellow-900/50 border border-yellow-700/50">
<div class="text-yellow-300 font-bold text-sm mb-2">Grooming</div>
<div class="space-y-1 text-gray-200">
<div>PM + Eng Lead groom</div>
<div class="text-gray-400">↓</div>
<div>Epic → Big Room Planning</div>
<div class="text-gray-400">↓</div>
<div>Story → Sprint</div>
<div class="text-gray-400">↓</div>
<div class="text-yellow-300 font-semibold">✓ Sprint Ready in Jira</div>
</div>
</div>

<div class="rounded p-3 bg-green-900/50 border border-green-700/50">
<div class="text-green-300 font-bold text-sm mb-2">Engineer</div>
<div class="space-y-1 text-gray-200">
<div class="font-mono text-green-400">/cxeng</div>
<div class="text-gray-400">↓</div>
<div>Adversarial review</div>
<div class="text-gray-400">↓</div>
<div>Build + TDD</div>
<div class="text-gray-400">↓</div>
<div class="font-mono text-green-400">/cxreview</div>
<div class="text-gray-400">↓</div>
<div class="text-green-300 font-semibold">✓ Preflight manifest</div>
</div>
</div>

<div class="rounded p-3 bg-orange-900/50 border border-orange-700/50">
<div class="text-orange-300 font-bold text-sm mb-2">QA Lead</div>
<div class="space-y-1 text-gray-200">
<div class="font-mono text-orange-400">/cxqa</div>
<div class="text-gray-400">↓</div>
<div>Publish to Sources</div>
<div class="text-gray-400">↓</div>
<div>SDET Automate</div>
<div class="text-gray-400">↓</div>
<div>Go / No-Go</div>
<div class="text-gray-400">↓</div>
<div class="text-orange-300 font-semibold">✓ PR created</div>
</div>
</div>

<div class="rounded p-3 bg-gray-700/50 border border-gray-600/50">
<div class="text-gray-300 font-bold text-sm mb-2">DevOps</div>
<div class="space-y-1 text-gray-200">
<div>Consume manifest</div>
<div class="text-gray-400">↓</div>
<div>UAT deploy</div>
<div class="text-gray-400">↓</div>
<div>Staging deploy</div>
<div class="text-gray-400">↓</div>
<div class="text-white font-semibold">✓ Production</div>
</div>
</div>

</div>

<div class="mt-4 text-center text-gray-400 text-xs">
Each handoff is an airlock. The next role can't start until the previous role's artifact is signed off.
</div>
