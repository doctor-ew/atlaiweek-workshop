---
layout: center
background: '#0d1117'
---

# Same App. Different Path.

<div class="text-sm text-gray-400 -mt-2 mb-6">Built twice — gstack's commands, then a spec-driven harness. Here's what diverged.</div>

<table class="w-full max-w-2xl mx-auto text-sm">
  <thead>
    <tr class="border-b border-gray-700">
      <th class="text-left pb-2 text-gray-400 font-normal w-36">What diverged</th>
      <th class="text-left pb-2 text-amber-400 font-semibold">gstack chose</th>
      <th class="text-left pb-2 text-blue-400 font-semibold">spec-driven chose</th>
    </tr>
  </thead>
  <tbody class="divide-y divide-gray-800">
    <tr>
      <td class="py-3 text-gray-300">Sidebar</td>
      <td class="py-3 text-gray-300">Inlined in <code class="bg-gray-800 px-1 rounded">HomeClient</code></td>
      <td class="py-3 text-gray-300">Extracted <code class="bg-gray-800 px-1 rounded">Sidebar.tsx</code></td>
    </tr>
    <tr>
      <td class="py-3 text-gray-300">Map markers</td>
      <td class="py-3 text-gray-300"><code class="bg-gray-800 px-1 rounded">TransitMarkers</code></td>
      <td class="py-3 text-gray-300">Boundary made explicit</td>
    </tr>
    <tr>
      <td class="py-3 text-gray-300">Prompt logic</td>
      <td class="py-3 text-gray-300">Inline in route handler</td>
      <td class="py-3 text-gray-300"><code class="bg-gray-800 px-1 rounded">lib/prompt.ts</code> (extracted)</td>
    </tr>
    <tr>
      <td class="py-3 text-gray-300">Types/schemas</td>
      <td class="py-3 text-gray-300"><code class="bg-gray-800 px-1 rounded">lib/types.ts</code> + <code class="bg-gray-800 px-1 rounded">lib/schemas.ts</code></td>
      <td class="py-3 text-gray-300"><code class="bg-gray-800 px-1 rounded">types/index.ts</code> + <code class="bg-gray-800 px-1 rounded">lib/matches.ts</code></td>
    </tr>
  </tbody>
</table>

<div class="mt-6 flex items-start gap-6">

<div class="text-center flex-1 pt-1">
  <span class="text-amber-400 font-semibold">Pragmatic</span>
  <span class="text-gray-500 mx-3">vs</span>
  <span class="text-blue-400 font-semibold">Modular</span>
  <div class="text-gray-300 mt-2 text-lg">Both got there. That's the point.</div>
</div>

<div class="border-l border-gray-700 pl-6 text-sm space-y-1 text-gray-400 shrink-0">
  <div class="text-gray-300 font-semibold text-xs uppercase tracking-wide mb-2">spec-driven also adds</div>
  <div>🔒 <span class="text-blue-300">Anti-spec-drift</span> — /drew-eng blocks hallucinated claims before code</div>
  <div>📖 <span class="text-blue-300">Works cited</span> — every spec fact points to a branch + commit + line</div>
  <div>📐 <span class="text-blue-300">Review gates</span> — SOLID · DRY · ACID · CoC · Big O checked at ship</div>
</div>

</div>
