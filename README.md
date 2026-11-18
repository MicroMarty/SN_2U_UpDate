# Steady Node firmware updates

## 0.1.96 — board-specific release

This release is exclusively for the board with USB runtime serial `42003B001650304B59383820` (ROM DFU `2073389B4B30`), signed by its previously approved board key. Other devices must not install it. Production signing trust is unchanged.

Stable manifest: https://micromarty.github.io/SN_2U_UpDate/latest.json

[Download the initial 0.1.96 SNP1 package](https://micromarty.github.io/SN_2U_UpDate/releases/0.1.96/SteadyNode-V2-0.1.96.snp)

Select this file through the device's local firmware-upload control for the initial installation. This version adds automatic descriptor checking on dashboard load and hourly while visible, a notification only for newer compatible firmware, and user-confirmed signed installation into the inactive slot. It never downloads a firmware just to compare versions.

Both slot images were compiled and their Ed25519 signatures verified. No physical boot validation was performed for 0.1.96. See releases/0.1.96/release.json for artifact hashes and signing-key fingerprint.

Only public firmware artifacts and release metadata belong here. No firmware source, private signing key, or provisioning image is distributed in this repository.
