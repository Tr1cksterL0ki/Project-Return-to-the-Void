# Windows configuration (safe, VALORANT-friendly)

This is a curated set of **low-risk** changes. It explicitly avoids:
- disabling Windows security (Defender, firewall)
- disabling kernel mitigations
- “debloat scripts” that break updates or components

## Keep Windows updated, but avoid preview updates
- Prefer normal monthly security updates.
- Skip optional “Preview” updates unless they fix a problem you have.
- If a bad patch hits, follow Microsoft’s Release Health / Known Issues for your Windows version.

## Background load: remove the real offenders
✅ Do
- Disable unnecessary startup apps (Task Manager → Startup)
- Uninstall unused RGB/peripheral suites and overlays (or stop them from auto-starting)
- Disable Xbox Game Bar *if you don’t use it*

⚠️ Consider
- Disable Search indexing **only if** you can see it causing disk/CPU activity during play

❌ Avoid
- Disabling Windows Update entirely
- Disabling Microsoft Defender entirely
- Renaming system executables (e.g., SmartScreen)

## Paging file
Don’t disable it. Some games still stutter without a page file even on high-RAM systems.

## Timer / “HPET” tweaks
Do not chase timer myths. Modern Windows timing behavior varies by build and hardware.
Only touch timer behavior if you can show a repeatable improvement in frametime/latency.

## Core isolation / Memory integrity (HVCI/VBS)
This is a security vs performance trade. For VALORANT, Vanguard restrictions can require security features depending on your environment:
- https://support-valorant.riotgames.com/hc/en-us/articles/22291331362067-Vanguard-Restrictions

If you change it, measure and keep a rollback plan.

## Useful built-in + legit tools
- Sysinternals Process Explorer: https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer
- Autoruns: https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns
