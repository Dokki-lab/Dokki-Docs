---
title: "Calendar Schedule Map"
canonical: "https://dokki.one/pub/docs/calendar-schedule-map"
source_url: "https://dokki.one/pub/docs/calendar-schedule-map"
updated_at: "2026-07-10T04:24:49.268+00:00"
generated_by: Dokki
---

# Calendar Schedule Map


Canonical source: [https://dokki.one/pub/docs/calendar-schedule-map](https://dokki.one/pub/docs/calendar-schedule-map)

```
import React from "react";
import { ArrowRight, CalendarClock, Pause, Play } from "lucide-react";
const frames=[["01","Schedule","An enabled cron schedule defines the next occurrence.",["Prompt","Cron","Timezone"]],["02","Project","Calendar expands future occurrences without storing separate events.",["Expand","Local day","Status"]],["03","Review","Completed work appears from agent run history.",["Run","Result","History"]]];
export default function CalendarScheduleMap(){const [active,setActive]=React.useState(0);const [paused,setPaused]=React.useState(false);React.useEffect(()=>{if(paused)return;const t=setInterval(()=>setActive(i=>(i+1)%frames.length),5200);return()=>clearInterval(t)},[paused]);const f=frames[active];return <main className="h-full min-h-0 overflow-hidden bg-[#f7f8f6] p-3 text-[#17201d] sm:p-4"><style>{"@keyframes calendarFrame{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}"}</style><section className="mx-auto flex h-full min-h-0 max-w-5xl flex-col overflow-hidden border border-[#d7ded8] bg-white shadow-sm" onMouseEnter={()=>setPaused(true)} onMouseLeave={()=>setPaused(false)} onFocusCapture={()=>setPaused(true)} onBlurCapture={()=>setPaused(false)}><header className="flex shrink-0 items-center justify-between gap-3 border-b border-[#d7ded8] px-4 py-3 sm:px-5"><div className="min-w-0"><div className="flex items-center gap-2 text-[10px] font-semibold uppercase tracking-[0.14em] text-cyan-700"><CalendarClock className="h-3.5 w-3.5"/>Calendar</div><h1 className="mt-1 truncate text-lg font-semibold sm:text-xl">Schedules become a readable timeline</h1></div><div className="flex items-center gap-1.5 text-[10px] text-[#68736d]">{paused?<Pause className="h-3.5 w-3.5 text-cyan-700"/>:<Play className="h-3.5 w-3.5 text-cyan-700"/>}<span className="hidden sm:inline">{paused?"Paused":"Auto-playing"}</span></div></header><div className="flex min-h-0 flex-1 flex-col sm:flex-row"><nav className="flex shrink-0 border-b border-[#d7ded8] sm:w-[34%] sm:flex-col sm:border-b-0 sm:border-r">{frames.map((item,i)=><button key={item[0]} onClick={()=>{setActive(i);setPaused(true)}} className={"flex flex-1 items-center gap-2 border-r px-3 py-2 text-left last:border-r-0 sm:border-b sm:border-r-0 "+(active===i?"bg-cyan-50":"text-[#68736d]")}><span className="text-[10px] font-semibold text-cyan-700">{item[0]}</span><span className="truncate text-xs font-medium sm:text-sm">{item[1]}</span></button>)}</nav><div key={active} className="flex min-h-0 flex-1 flex-col justify-between gap-3 p-4 sm:p-5" style={{animation:"calendarFrame 360ms ease both"}}><div><p className="text-[10px] font-semibold uppercase tracking-[0.14em] text-cyan-700">Step {f[0]}</p><h2 className="mt-1 text-xl font-semibold sm:text-2xl">{f[1]}</h2><p className="mt-2 text-sm leading-5 text-[#52605a] sm:text-base sm:leading-6">{f[2]}</p></div><div className="flex flex-wrap items-center gap-2">{f[3].map((x,i)=><React.Fragment key={x}><span className="border border-[#d7ded8] bg-[#f7f8f6] px-2.5 py-1 text-xs font-medium">{x}</span>{i<f[3].length-1&&<ArrowRight className="h-3.5 w-3.5 text-cyan-600"/>}</React.Fragment>)}</div><div className="flex items-center justify-between border-t border-[#e5e9e5] pt-3"><div className="flex gap-1.5">{frames.map((x,i)=><button key={x[0]} onClick={()=>{setActive(i);setPaused(true)}} className={"h-1.5 rounded-full "+(active===i?"w-7 bg-cyan-600":"w-1.5 bg-[#c6cec8]")}/>)}</div><button onClick={()=>{setPaused(true);setActive((active+1)%frames.length)}} className="text-xs font-semibold text-cyan-700">Next</button></div></div></div></section></main>}
```

---

Published from Dokki.
