# Three Decisions That Shaped the App

<div class="mt-6 space-y-5">

<div class="flex gap-6 items-start">
  <div class="text-amber-400 font-bold text-2xl w-8 shrink-0">1</div>
  <div>
    <div class="font-semibold">inject_delay via POST body, not URL param</div>
    <div class="text-gray-300 text-sm mt-1">Client reads <code>?inject_delay=gold_line</code>, forwards it in the API body. Clean separation. The URL triggers; the server routes.</div>
  </div>
</div>

<div class="flex gap-6 items-start">
  <div class="text-amber-400 font-bold text-2xl w-8 shrink-0">2</div>
  <div>
    <div class="font-semibold">No SWR polling — server fetches MARTA inline</div>
    <div class="text-gray-300 text-sm mt-1">Background polling is wasted work. MARTA data is fetched when Claude needs it, not continuously. The map uses its own 10s poll for vehicle positions.</div>
  </div>
</div>

<div class="flex gap-6 items-start">
  <div class="text-amber-400 font-bold text-2xl w-8 shrink-0">3</div>
  <div>
    <div class="font-semibold">8s timeout → pre-baked fallback (not an error)</div>
    <div class="text-gray-300 text-sm mt-1">Conference wifi is hostile. If Claude doesn't respond in 8 seconds, a human-written fallback renders. The user never sees a spinner forever.</div>
  </div>
</div>

</div>
