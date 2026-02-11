# Measurement & test workflow (VALORANT-focused)

This repo is **measurement-first**. If you can’t measure it, treat it as a hypothesis.

## Tools
- **Frame times:** PresentMon / CapFrameX (frametime graphs + 1%/0.1% lows)
- **System latency (supported titles):** NVIDIA FrameView “PC Latency”
- **Network:** VALORANT in-game graphs (ping, packet loss, jitter feel), plus PingPlotter/WinMTR for path testing
- **Stability:** Event Viewer (WHEA, driver resets), HWiNFO (thermals/throttling)

## A/B methodology (non-negotiable)
1. **Baseline**
   - Same map/mode (e.g., Range + a DM/TDM) for 10–15 minutes
   - Same graphics settings, same cap
   - Capture a frametime run
2. **Change exactly ONE thing**
3. **Re-test** same scenario
4. **Keep only if**
   - spike frequency decreases and/or 1%/0.1% lows improve **and**
   - no new crashes, USB drops, audio pops, or Vanguard complaints
5. **Rollback** immediately on regression

## What “good” looks like in VALORANT
- Flat frametime plot (few spikes)
- 1% lows close to average FPS
- Packet loss ~0 on a stable connection
- No recurring WHEA errors or driver resets

## Common placebo traps
- Changing 10 settings at once
- Using LatencyMon numbers as a universal “game latency score” (it’s primarily a DPC/ISR diagnostic tool)
- Judging “hitreg” feel without controlling for peeker’s advantage + packet loss + frametime variance

## Recommended experiment order (Void's PC: 5700X + 4060)
1) Fix packet loss / Wi‑Fi issues (Ethernet, router placement, buffering settings)
2) Reflex ON + stable FPS cap
3) Remove background bloat (startup apps, overlays)
4) Optional: GPU undervolt (conservative) to stabilize clocks
5) Optional: Ryzen PBO2 + Curve Optimizer (stability tested)

