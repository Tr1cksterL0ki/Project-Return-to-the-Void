# Do-not-use list (unsafe / low-value for VALORANT)

These show up in “tweak culture” a lot. They are either:
- security regressions
- anti-cheat hostile
- or too unstable / low ROI

## Kernel / driver security bypasses
❌ Do not disable the Microsoft Vulnerable Driver Blocklist to run tools like RWEverything.
- Microsoft KB: https://support.microsoft.com/en-gb/topic/kb5020779-the-vulnerable-driver-blocklist-after-the-october-2022-preview-release-3fcbe13a-6013-4118-b584-fcfbc6a09936

❌ Do not use RWEverything-based scripts to change xHCI IMOD for a gaming PC.

## Security “optimizations”
❌ Do not disable Microsoft Defender or the firewall for “performance.”
❌ Do not disable exploit mitigations, VBS/HVCI, or CPU security mitigations as a default.

## Networking myths
❌ Port-forwarding does not “reduce ping” on a healthy connection. Do it only for connectivity troubleshooting.
Riot port forwarding guidance: https://support-valorant.riotgames.com/hc/en-us/articles/4402306473619-How-to-Set-Up-Port-Forwarding

## Folklore fixes
❌ Blindly downgrading Visual C++ runtimes to “fix hitreg” (treat corruption by reinstalling official runtimes instead).
❌ “Clear standby list every 5 minutes” scheduled tasks.
