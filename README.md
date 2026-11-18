# Steady Node firmware update test

## 0.1.97 -> 0.1.98

This test pair is exclusively for board ROM DFU `2073389B4B30`, USB runtime serial `42003B001650304B59383820`, signed by its existing approved board key. Production trust is unchanged.

1. The owner installs the locally prepared **0.1.97 sparse provisioning HEX** using USB/DFU.
2. Open the Steady Node dashboard with browser Internet access: it announces **0.1.98**.
3. Open Firmware, click **Check for updates**, then confirm **Install signed update**.
4. After restart the device should report **0.1.98**; another check should report that firmware is up to date.

Stable manifest: https://micromarty.github.io/SN_2U_UpDate/latest.json

Both versions include a visible error when the update server is unreachable. Their source differs only in version numbers. Checking downloads only the small descriptor; installation downloads one signed inactive-slot bundle (209993 bytes).

[0.1.98 local-upload package](https://micromarty.github.io/SN_2U_UpDate/releases/0.1.98/SteadyNode-V2-0.1.98.snp)

Both slots, signatures, image hashes, reset vectors, browser tests and a simulated relay using the real binaries have been checked. Physical flash and boot validation are left to the owner. See releases/0.1.98/release.json for artifact hashes.

Only signed public update artifacts and release metadata are published. No private keys, firmware source or DFU provisioning image is included.
