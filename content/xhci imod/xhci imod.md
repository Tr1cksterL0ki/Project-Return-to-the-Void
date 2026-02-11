# xHCI Interrupt Moderation (IMOD) — removed for safety

Older latency-tweak communities sometimes recommend changing xHCI interrupt moderation registers (IMOD) using tools like **RWEverything**.

For a competitive VALORANT PC, this repo **does not recommend** that approach because it typically requires weakening Windows kernel protections or loading vulnerable drivers, which is:
- a **security risk**
- potentially **anti-cheat hostile** (Vanguard environment integrity)
- not well-supported by reproducible end-to-end latency measurements for modern Windows builds

See: https://github.com/Tr1cksterL0ki/Project-Return-to-the-Void/blob/main/docs/do_not_use.md

## Safer alternatives
If you’re troubleshooting USB input instability:
- move wireless dongles away from USB 3.x interference (use a USB2 extension)
- try different motherboard ports (avoid chained hubs)
- remove heavy peripheral suites/overlays during play
- update chipset/USB controller drivers and BIOS

If you have proven USB driver latency issues (rare), treat it as a **driver/firmware stability problem**, not a “registry hack” problem.
