---
title: "Editor Capability Map"
canonical: "https://dokki.one/pub/docs/editor-capability-map"
source_url: "https://dokki.one/pub/docs/editor-capability-map"
updated_at: "2026-07-10T04:19:43.335+00:00"
generated_by: Dokki
---

# Editor Capability Map


Canonical source: [https://dokki.one/pub/docs/editor-capability-map](https://dokki.one/pub/docs/editor-capability-map)

```
import React from "react";
import { ArrowRight, Pause, Play, Sparkles } from "lucide-react";
const frames = [["01","Start","Create structure with slash commands and blocks.",["Open","Choose","Create"]],["02","Understand","Bring in context with mentions and embeds.",["Inspect","Check","Continue"]],["03","Finish","Use selection controls and Copilot to refine.",["Review","Apply","Share"]]];
export default function VisualGuide() {
  const [active, setActive] = React.useState(0);
  const [paused, setPaused] = React.useState(false);
  React.useEffect(() => {
    if (paused) return;
    const timer = setInterval(() => setActive((index) => (index + 1) % frames.length), 5200);
    return () => clearInterval(timer);
  }, [paused]);
  const frame = frames[active];
  const select = (index) => { setActive(index); setPaused(true); };
  return <main className="h-full min-h-0 overflow-hidden bg-[#f7f8f6] p-3 text-[#17201d] sm:p-4">
    <style>{"@keyframes dokkiFrame {from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}"}</style>
    <section className="mx-auto flex h-full min-h-0 max-w-5xl flex-col overflow-hidden border border-[#d7ded8] bg-white shadow-sm" onMouseEnter={() => setPaused(true)} onMouseLeave={() => setPaused(false)} onFocusCapture={() => setPaused(true)} onBlurCapture={() => setPaused(false)}>
      <header className="flex shrink-0 items-center justify-between gap-3 border-b border-[#d7ded8] px-4 py-3 sm:px-5">
        <div className="min-w-0"><div className="flex items-center gap-2 text-[10px] font-semibold uppercase tracking-[0.14em] text-orange-700"><Sparkles className="h-3.5 w-3.5 shrink-0"/>Document Editor</div><h1 className="mt-1 truncate text-lg font-semibold leading-tight sm:text-xl">Write, reference, and refine</h1></div>
        <div className="flex shrink-0 items-center gap-1.5 text-[10px] text-[#68736d]">{paused ? <Pause className="h-3.5 w-3.5 text-orange-700"/> : <Play className="h-3.5 w-3.5 text-orange-700"/>}<span className="hidden sm:inline">{paused ? "Paused" : "Auto-playing"}</span></div>
      </header>
      <div className="flex min-h-0 flex-1 flex-col sm:flex-row">
        <nav aria-label="Story steps" className="flex shrink-0 border-b border-[#d7ded8] sm:w-[34%] sm:flex-col sm:border-b-0 sm:border-r">{frames.map((item, index) => <button key={item[0]} onClick={() => select(index)} className={"flex min-w-0 flex-1 items-center gap-2 border-r px-3 py-2 text-left transition-colors last:border-r-0 sm:border-b sm:border-r-0 sm:last:border-b-0 " + (active === index ? "bg-orange-50 text-[#17201d]" : "bg-white text-[#68736d] hover:bg-[#f7f8f6]")}><span className={"text-[10px] font-semibold " + (active === index ? "text-orange-700" : "text-[#9aa49e]")}>{item[0]}</span><span className="truncate text-xs font-medium sm:text-sm">{item[1]}</span></button>)}</nav>
        <div key={active} className="flex min-h-0 flex-1 flex-col justify-between gap-3 p-4 sm:p-5" style={{animation:"dokkiFrame 360ms ease both"}}>
          <div><p className="text-[10px] font-semibold uppercase tracking-[0.14em] text-orange-700">Step {frame[0]}</p><h2 className="mt-1 text-xl font-semibold leading-tight sm:text-2xl">{frame[1]}</h2><p className="mt-2 max-w-2xl text-sm leading-5 text-[#52605a] sm:text-base sm:leading-6">{frame[2]}</p></div>
          <div className="flex flex-wrap items-center gap-2">{frame[3].map((label, index) => <React.Fragment key={label}><span className="border border-[#d7ded8] bg-[#f7f8f6] px-2.5 py-1 text-xs font-medium">{label}</span>{index < frame[3].length - 1 && <ArrowRight className="h-3.5 w-3.5 text-orange-600"/>}</React.Fragment>)}</div>
          <div className="flex items-center justify-between gap-3 border-t border-[#e5e9e5] pt-3"><div className="flex gap-1.5">{frames.map((item, index) => <button key={item[0]} aria-label={"Show step " + item[0]} onClick={() => select(index)} className={"h-1.5 rounded-full transition-all " + (active === index ? "w-7 bg-orange-600" : "w-1.5 bg-[#c6cec8]")}/>)}</div><button onClick={() => { setPaused(true); setActive((active + 1) % frames.length); }} className="flex items-center gap-1 text-xs font-semibold text-orange-700">Next <ArrowRight className="h-3.5 w-3.5"/></button></div>
        </div>
      </div>
    </section>
  </main>;
}
```

---

Published from Dokki.
