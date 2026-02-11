# BIOS / UEFI baseline (Ryzen 7 5700X)

Goal: stable boosts, stable memory, no thermal throttling.

## Always do
- Update BIOS to a stable release for your board
- Enable your RAM profile (**DOCP/XMP**) and validate stability
- Enable **Above 4G Decoding** + **Resizable BAR** (if supported)
- Keep **UEFI mode** (no CSM) if you’re on Windows 11 / VALORANT (Secure Boot requirements)

## Ryzen tuning (optional)
### PBO2 + Curve Optimizer
- Can improve sustained boost and reduce temps, which can help consistency.
- Go conservative. Validate with long gaming sessions + a stability test.
- Watch for WHEA errors (Event Viewer).

## Power / idle states
Avoid blanket “disable all C-states” recommendations.
Only consider power-state changes if you have proven wake-latency spikes and you have thermal headroom.

## fTPM / Secure Boot for VALORANT
Riot’s Vanguard restrictions for Windows 11 generally require TPM 2.0 + Secure Boot:
https://support-valorant.riotgames.com/hc/en-us/articles/22291331362067-Vanguard-Restrictions
