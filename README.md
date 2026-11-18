# Steady Node — Safari compatibility test

## Install 0.1.101 locally, then test 0.1.102 online

The 0.1.99 page can report an unreachable update server on the owner's iPad/iPhone Safari although a fresh direct manifest link opens. These are compatibility candidates for a physical Safari test; the original Safari failure has not yet been reproduced directly by the agent.

1. [Download signed 0.1.101 SNP1 package](https://micromarty.github.io/SN_2U_UpDate/releases/0.1.101/SteadyNode-V2-0.1.101.snp) to Files/Downloads.
2. On the device's Firmware page, use **Local file** → choose that file → **Install local file**. Confirm once and wait for restart.
3. Verify **0.1.101**, then choose **Check for updates**. The server candidate is **0.1.102**.

The candidates use simple HTTPS CORS GETs, omit cookies and custom request headers, refresh the descriptor via a URL token, and use bounded XMLHttpRequest reads if fetch fails. CORS and TLS remain enforced. No upload is automatically retried. USB-status, release-information, timeout and network errors have separate messages.

Stable manifest: https://micromarty.github.io/SN_2U_UpDate/latest.json

[0.1.102 local package](https://micromarty.github.io/SN_2U_UpDate/releases/0.1.102/SteadyNode-V2-0.1.102.snp)

Both versions are exclusively for ROM DFU board `2073389B4B30` / runtime `42003B001650304B59383820`, using its existing approved signing key. Production trust is unchanged. Sources differ only in version numbers. See releases/0.1.102/release.json for hashes and test scope.
